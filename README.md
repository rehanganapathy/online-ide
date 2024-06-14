# online-ide


This app allows you to run your code online, similar to what replit does. This approach uses kubernetes and an orchestrator to spin up pods based on the language selected(either nodejs or python), s3 is used to store all the data. On initialising a new workspace, base code is displayed to the user. Pty has been used for pseudo terminal, and a dockerfile has also been written to initialise the pods. Here is an image of the approach:


![Untitled Diagram](https://github.com/rehanganapathy/online-ide/assets/79349712/0cbc33e2-d2dd-4875-a0e7-53758fd36c2e)


To run this, make sure you have an online kubernetes cluster running(could use GCP or vultr), specify the urls for ingress and add the base code to s3. To add more security you could add a proxy server, and add another pod for each pod created and run the terminal on your second pod to prevernt your s3 info from getting leaked. 
