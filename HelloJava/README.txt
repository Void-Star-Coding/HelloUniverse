                                                                              
Part 1                                                                        
                                                                              
1. Download the Java Development kit for your system                          
  https://www.oracle.com/java/technologies/downloads/                         
                                                                              
2. Download and install preferred IDE (IntelliJ)                              
  https://www.jetbrains.com/idea/                                             
  * Optionally add to environment variables for running raw from console      
                                                                              
3. Open IntelliJ (                                                            
  a. Create a New Project                                                     
   * If unnamed token error appears but the projects run,                     
      Click File -> Repair IDE                                                
      Keep clicking continue in the bottom right                              
                                                                              
   b. In file Main:                                                           
                                                                              
      void main() {                                                           
        IO.println("Hello Java!");                                            
      }                                                                       
                                                                              
    c. Shift+F10 to run                                                       
    d. CTRL+SHIFT+ALT+S to open Project Structure to begin exporting as a .jar
        Project Settings -> Artifacts -> (+) icon -> JAR -> From modules with dependencies
        Main Class: Main             
        Click ok, then ok again                                                       
                                                                              
    e. Alt+B -> Build Artifacts
        HelloJava -> Build
        HelloJava.jar should show up in out\artifacts\HelloJava_jar

4. Navigate to the folder containing the project
  * C:\Users\<username>\IdeaProjects\HelloJava\out\artifacts\HelloJava_jar
    RClick or Shift+RClick -> open Terminal
    Inside terminal
      $ java -jar .\HelloJava
    The output should be
      > Hello Java!
                                                                              
                                                                              
                                                                              
                                                                              
                                                                              
                                                                              
                                                                              
                                                                              