# **Java Build and Execution Automation with Jenkins**

This repository automates the process of **compiling** and **running** a Java program using Jenkins. The Jenkins pipeline defined in the `Jenkinsfile` automates the following:

- **Compiling the Java file**: The Java source code is compiled automatically.
- **Running the Java program**: The compiled Java program is executed.
- **Capturing the output**: The output of the program is saved to a `result.txt` file.




## **What It Does**
- Automatically **clones** the GitHub repository.
- **Compiles** the Java file (`ex.java`).
- **Runs** the compiled Java program and redirects the output to a file (`result.txt`).
- **Archives** the result in Jenkins for review.


### Check the jenkins script here
- [jenkins file ](https://github.com/Gayathri39103/demo_java/blob/main/Jenkinsfile) 

### Jenkins documentation to refer!
- [Jenkins Documentation](https://www.jenkins.io/doc/)  <!-- Link to Jenkins documentation -->
