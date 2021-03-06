# Build your First Twitter Bot

In this group project, we'll be using our Ruby skills to build out our very own Twitter Bots - programs that automatically update a twitter account of our choice. To do this, we'll need to use the Twitter API (wia the 'twitter' gem) and Heroku.

API stands for *Application Programming Interface*. APIs are the way that apps can talk to each other over the internet. Every time you log in to a site using your facebook credentials, or access data from one app on another application, you're using APIs. Twitter's API is especially good - it's well documented and lets you do everything you'd be able to do on it's web interface.

 By the end of this project, you'll have a bot that updates twitter automatically, at set intervals of time.

##Examples
Check out these examples of great Twitter bots:
+ [@pentametron](https://twitter.com/pentametron?lang=en) - Retweets in Iambic Pentameter
+ [@everyword](https://twitter.com/everyword) - Tweets every word in the English Language
+ [The best bots of 2015](http://qz.com/279139/the-17-best-bots-on-twitter/)

## Ideation
Take 5 minutes with your team to pick a process that you want to try and automate with your bot. What will it do? How will it work? What will it be called?

## Setup
Now that you've decided on a goal for your bot, follow these setup instructions to get started!
+ Fork and Clone this Repository! In the repository you'll see the following files:
  + app.rb: This is where you'll be writing the code that powers your bot
  + Gemfile: This is where we store the gems that we'll be using to build our appliation. We're using the 'twitter' gem as an API wrapper, and the 'dotenv' gem to protect our twitter credentials.
+ Choose your twitter bot's name and register it on [www.twitter.com](Twitter).
+ Head to [apps.twitter.com] and choose the 'Create a New App Button' - Fill in you application's details and agree to the terms and conditions.
+ In your repository, create a file called `.env`. In the file, add the following code:

```ruby
CONSUMER_KEY = "your consumer key"
CONSUMER_SECRET = "your consumer secret"
ACCESS_TOKEN = "your access token"
ACCESS_TOKEN_SECRET = "your access token secret"
```

+ Your consumer key, consumer secret, access token, and access token secret can all be found on the app page that you opened at apps.twitter.com under 'Keys and Access Tokens'. To get an access token, click on "Generate my Access Token and Access Token Secret". Paste all of these keys and tokens into the correct place in your .env file.

## Bot Making Time!

Check out the documentation for the Twitter Gem: [https://github.com/sferik/twitter]. 

In your app.rb file, take some time to get acquainted with the 'twitter' gem's capabilities. For example, if you want to tweet directly from the gem, run:

```
client.update("I'm tweeting from the command line!")
```

Figure out how to:
- Follow a user
- See a user's last ten tweets
- Get a list of a user's followers
- Get a link to a user's profile image
- Get a list of trending topics

To run your program (to test it), run `ruby app.rb` from the command line.

Now, take your time and build out your twitter bot! Remember to figure out the logic of what you want to do before writing the code.

Make sure to push all of your code back up to Github!

## Deploy to Heroku!
Now that you have a Twitter bot that works locally, it's time to put it online so that it runs automatically! Follow these instructions:
+ If you don't have a [Heroku](https://www.heroku.com/) account yet, sign up. Otherwise, log in to your dashboard.
+ Create a new app.
+ Connect your app to the github repo under the "Deploy" tab, and then deploy!
+ heroku scheduler...