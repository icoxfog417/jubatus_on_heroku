# Jubatus on Heroku
Demo of running Jubatus on Heroku.

## How to run

1. Edit the `run_jubatus` script to run the jubatus.
2. After deploy to the heroku, run the process by `heroku ps:scale worker=1`
3. After running the Jubatus process in step 2, then run main process.

It requires 2 process (one is for Jubatus, the other is your application that uses Jubatus), so you have to prepare 2 dyno (it's not free).
The process is defined in the `Procfile`, so you can customize the name or script.

In the demo, I use Python script (`tutorial.py`).  
But you can use other language, because [Jubatus supports multiple language client](http://jubat.us/en/quickstart.html#install-jubatus-client-libraries).  

If you use other language, please chage python buildpack in `.buildpacks` to [your language buildback](https://devcenter.heroku.com/articles/buildpacks).
