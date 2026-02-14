This lab uses GitHub Actions to show how automated workflows work in real projects. 
A workflow is simply a set of automated steps that run when something happens in your repository, like a push or a pull request. 
Instead of manually building or testing code, GitHub can do it for you on its own virtual machines.

In Workflow 1 (Dependent Jobs), you demonstrate job order using needs. 
The build job runs first, the test job waits for build to finish, and deploy waits for test. This mimics real software pipelines where you must build code before testing it, and test it before deploying.
The needs keyword is what enforces this order.

In Workflow 2 (Multi-Platform Testing), the goal is to show parallel execution. 
Since no needs keyword is used, all jobs run at the same time. Each job runs on a different operating system (Ubuntu, Windows, macOS) to confirm that the project works across platforms. 
This is important because software can behave differently on different OS.

Key concepts include runs-on (chooses the operating system), steps (individual tasks inside a job), and needs (controls job order). 
Together, these features simulate a simple CI/CD pipeline where code is automatically built and tested whenever changes are made.

Overall, this lab teaches how automation improves reliability and saves time. 
Instead of manually checking everything, workflows ensure your code is consistently built and tested, which is exactly how modern development teams maintain quality.
