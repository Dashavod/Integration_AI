for work with google function we need module
``functions-framework 

And we can use this repository for base your
[template repo](https://github.com/stefanbertos/for-developers-gcp-cloud-function-python)

- Before deploy you update your `requirements.txt`, if you add new modules or change version,
- Always delete unusual import in your code
- And in cloud enviroument, you don't need credential for google service, you enabled necessary api, and give their servise account necessary permission