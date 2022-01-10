# Launch applications
I opened a terminal window for each application. I used gradlew for launching them.

## Registration 
Command:
```bash
./gradlew registration:bootRun
```
Logs:
![spring](https://user-images.githubusercontent.com/46299278/148803519-4b7b6e48-c1f1-4567-8547-d152685d6c95.png)


## accounts 
Command:
```bash
./gradlew :accounts:bootRun
```
Logs:
![accounts1](https://user-images.githubusercontent.com/46299278/148802669-4f7435a9-7a67-47fa-a7dc-682e2eaa91bc.png)
![accounts2](https://user-images.githubusercontent.com/46299278/148802695-00bee83a-e275-420c-8bc6-a04979871f2b.png)
## Web
Command:
```bash
./gradlew :web:bootRun
```
Logs:

![web1](https://user-images.githubusercontent.com/46299278/148803338-e924155c-354c-448a-b8af-0e280bf9d83b.png)
![web2](https://user-images.githubusercontent.com/46299278/148803346-debc8fde-a2ea-4bd2-9f31-39dd5d67990e.png)

# Registration
We can see on the dashboard how both application are registered
![eureka1](https://user-images.githubusercontent.com/46299278/148803736-4bc91685-a728-4e65-ab13-48dbaffbe629.png)

## Adding a replica
A replica was added changing the port on the file ```accounts/src/resources/application.yml```. After it, another terminal was opened and an accounts application was launched.
The logs were:
![secondAccount](https://user-images.githubusercontent.com/46299278/148804213-151b7688-5776-41e2-8ac0-9d88e9b0ab53.png)

![secondAccount2](https://user-images.githubusercontent.com/46299278/148804230-110dc306-5b07-4953-9c5f-731bd6746a0c.png)

And in the dashboard we get that 2 replicas were up:
![twoAccountsDashboard+](https://user-images.githubusercontent.com/46299278/148804305-06cec7bb-da6c-493b-827d-b0c5fee01e22.png)

# Destroying a replica
for destroying the replica on the port 2222 we just preshed  ctrl+C, we could see on the dashboard how it detected it and remove it from the registered services:
![killed](https://user-images.githubusercontent.com/46299278/148804686-cd842eac-282a-469f-ab23-de7b5be339c6.png)

We tried to use the web and all just works, the reason is because the web gets the service accounts from eureka and it give it the one alive.



![web](https://user-images.githubusercontent.com/46299278/148804829-87ce5c95-44e8-4980-9725-5480b0ae6c2f.png)




![keri](https://user-images.githubusercontent.com/46299278/148804837-faffa2fc-95bf-4cee-9831-beeaa8f159c0.png)



