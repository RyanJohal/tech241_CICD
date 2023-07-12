# Linking jenkins job to github repo
![Alt text](<images/Screenshot 2023-07-11 135611.png>)
1. create job
2. Select github project box and enter repo https link.
![Alt text](<images/Screenshot 2023-07-11 133454.png>)
3. Restrict where project is ran so that node doesn't get overloaded.
![Alt text](<images/Screenshot 2023-07-11 133637.png>)
4. In source code management select git and paste ssh link from github.
5. Add private ssh key and ensure file name matches.
6. Change branch to main
7. In build environment select Provide Node & npm bin/ folder to PATH, and choose Sparta-Node-JS.
![Alt text](<images/Screenshot 2023-07-11 135253.png>)
8. Select add build step, execut shell. 
9.  Enter cd app, npm install, npm test
![Alt text](<images/Screenshot 2023-07-11 135428.png>)
10. Save and build.

# Adding webhook to jenkins
1. On Jenkins select configure on job you wish to add webhook.
2. Go to build triggers and select GitHub hook trigger for GITScm polling
3. Save changes
4. On github repo select settings and go to webhooks.
5. Add webhook
6. Enter ```http://18.133.222.223:8080/github-webhook/``` into payload url
7. Content type application/json
8. Select push and pull to trigger webhook
9. Ensure active box is selected at the bottom
10. Create webhook
11. Commit changes to repo to test whether it has worked.

# Merge branches with jenkins
1.  Same steps as creating a job
2.  Enter dev branch
3.  Add additional behaviours 'merge before build'
4.  Enter origin in repository and main in branch to merge to
![Alt text](<images/Screenshot 2023-07-12 142437.png>)
5. Add post build actions, git publisher.
6. Select push only if build succeeds and merge results.
7. Add branches.
8. Enter branch to push main.
9. Enter target remote name main.
![Alt text](<images/Screenshot 2023-07-12 142458.png>)
10. Build other projects, next project in the pipeline.
![Alt text](<images/Screenshot 2023-07-12 142512.png>)

# Delivering changes to aws
1. Create job ![Alt text](<images/Screenshot 2023-07-12 144050.png>)
![Alt text](<images/Screenshot 2023-07-12 144118.png>)
2. Add build, execute shell
![Alt text](<images/Screenshot 2023-07-12 144138.png>)