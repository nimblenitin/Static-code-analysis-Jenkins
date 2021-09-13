# Static-code-analysis-Jenkins

The Jenkins Next Generation Warnings plugin collects compiler warnings or issues reported by static analysis tools and visualizes the results.

Steps to integrate and configure static code analysis tools like Checkstyle, Pmd, and FindBugs with Jenkins.

```

1. Add the Warnings Next Generation plugin under Manage Jenkins.

2. Create a Maven Job and add the below SCM source-
https://github.com/jenkins-docs/simple-java-maven-app

3. Click on the add a post build step and select invoke top level maven targets from the list. Select the maven version that you have configured in jenkins. Specify the goals as: clean install checkstyle:checkstyle pmd:pmd findbugs:findbugs

4. Click on post build actions. You will see an option Record compiler warnings and static analysis results in the drop down list if you have correctly installed the warnings next generation plugin. Select this option. Add the Checkstyle, CMD and Findbugs tool.

5. Save and build the Job. On clicking on the build number you will be able to see the report for all three tools- Checkstyle, CMD and Findbugs.

```
