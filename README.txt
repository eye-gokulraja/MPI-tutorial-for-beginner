# MPI-tutorial-for-beginner
A Sample program to show how MPI works.

========================================================HOW TO========================================================
  1.Download the High performance computing(HPC) SDK pack
      https://msdn.microsoft.com/en-us/library/cc853440(v=vs.85).aspx
  2.Install the HPC SDK 
      ***************NOTE***************
          I installed the HPC SDK 2008
      **********************************
  3.Install visual studio IDE
      https://www.visualstudio.com/vs/visual-studio-express/
      ***************NOTE***************
          Community edition is free to use,so download that
      **********************************
  4.Open visual studio IDE
      In the toolbar,click on Tools->Get Tools and Features...
      ***************NOTE***************
          Click yes on the prompting window,this will open visual studio installer
      **********************************
  5.In Windows section,Select Desktop Development with C++
  6.In the right bottom,modify button will be enabled.click it
      ***************NOTE***************
          close all visual studio windows to start installation
      **********************************
  7.Lauch the visual studio
  8.Create a new project
      File->New->Project
  9.In Visual C++ section,choose General,select Empty project
  10.Change name,location,solution name if needed and click ok
      ***************NOTE***************
          leave the solution to be "Create new solution"
      *********************************
  11.In the Right side you will see Solution Explorer
      ***************NOTE***************
          If not,go to View->Solution Explorer
      **********************************
  12.Solution Explorer will show your project files
  13.IN Source Files section,Right click and go to Add->New item->C++ File
      ***************NOTE***************
          In Visual C++ Section  
      **********************************
  14.Choose a name if needed and click Add
  15.This will open your C++ File
  16.Now,Right click on your project name in Solution Explorer,Click on properties
  17.change the following
    *)Configuration Properties->Linker->System
        select the SubSystem as Console (/SUBSYSTEM:CONSOLE)
        ***************NOTE***************     
                    Refer change1.png
        **********************************
    *)Configuration Properties->Linker->General
        select the Additional Library Directories as <path>
              <path> where you have installed HPC SDK pack->Lib->i386  
              ***************NOTE***************     
                    Usually in C:\Program Files\Microsoft HPC Pack 2008 SDK\Lib\i386
                    Refer change4.png
              **********************************
    *)Configuration Properties->Linker->Input
         select the Additional Dependencies as msmpi.lib
              ***************NOTE***************     
                    If lot of stuff are already in that area,add it to the last with a semi colon
                    Refer change2.png
              **********************************
     *)Configuration Properties->C/C++->General
         select the Additional Include Directories as <path>
                <path> where you have installed HPC SDK pack->Include  
              ***************NOTE***************     
                    Usually in C:\Program Files\Microsoft HPC Pack 2008 SDK\Include
                    Refer change3.png
              **********************************
  18.Type your mpi code,right click on project name in Solution Explorer and then Click Build
  19.To run the mpi code,do the following
         Open Command prompt by pressing windows key,type cmd,press enter.
         navigate to your project location
         ***************NOTE***************     
            cd .. to go back 
            cd <folder_name> to go into folder
            dir to display current directory contents
         **********************************
         when you are inside your project folder
         go to Debug and type the command
                  mpiexec -n <number_of_process> <filename.exe>
         Ouput will be displayed
         ***************NOTE***************     
                    Refer output.png
         **********************************
