For create google function, we must have billing google project. In Google cloud console choose, Google functions and then "Create function". In this form choose a nearest region?, setup trigger for your function, in section Runtime you can enter your enviroument variables, and options.

![[Pasted image 20230303161517.png]]

In next page
![[Pasted image 20230303162417.png]]

Google provide us simple function template, with entrypoint helloword
Import your code from cloud source repository, which connected for your github repository 
***Your entrypoint must be the same***
Click Deploy, wait some time and test your new function

Also you can create function by the shell, but you don't have so much options
 ``` shell
gcloud auth login
gcloud config set project PROJECT_ID
gcloud functions deploy hello_world --region europe-west3 --allow-unauthenticated --memory 128MB --runtime python39 --timeout 90 --min-instances 0 --max-instances 1 --trigger-http --service-account hello-world-function-sa@for-developers-343319.iam.gserviceaccount.com 
```
