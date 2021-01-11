![Phoenix](https://telegra.ph/file/3ef6e9ace5a18fab42bda.jpg)
# Phoenix
[![forthebadge made-with-python](http://ForTheBadge.com/images/badges/made-with-python.svg)](https://www.python.org/)
[![ForTheBadge built-with-love](http://ForTheBadge.com/images/badges/built-with-love.svg)](https://GitHub.com/MrHonekawa/)</br>

![Python Version](https://img.shields.io/badge/python-3.8.3-green?style=for-the-badge&logo=appveyor)
![Issues](https://img.shields.io/github/issues/MrHonekawa/Phoenix?style=for-the-badge&logo=appveyor)
![Forks](https://img.shields.io/github/forks/MrHonekawa/Phoenix?style=for-the-badge&logo=appveyor)
![Stars](https://img.shields.io/github/stars/MrHonekawa/Phoenix?style=for-the-badge&logo=appveyor)
![LICENSE](https://img.shields.io/github/license/MrHonekawa/Phoenix?style=for-the-badge&logo=appveyor)
![Contributors](https://img.shields.io/github/contributors/MrHonekawa/Phoenix?style=for-the-badge&logo=appveyor)
![Repository Size](https://img.shields.io/github/repo-size/MrHonekawa/Phoenix?style=for-the-badge&logo=appveyor)</br>

[![Join Support!](https://img.shields.io/badge/TG%20SUPPORT-CHAT)](https://t.me/TGBOTSUPPORT)
[![Codacy Badge](https://app.codacy.com/project/badge/Grade/cfb691a93a064d9ea753ef2b5fccf797)](https://www.codacy.com/manual/MrHonekawa/Phoenix?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=MrHonekawa/Phoniex&amp;utm_campaign=Badge_Grade)

A modular telegram Python bot running on python3 with an sqlalchemy database.
Can be found on telegram as [Phoenix](https://t.me/).

The Support group can be reached out to at [TG BOT SUPPORT](https://t.me/TGBOTSUPPORT), where you can ask for help setting up your bot, discover/request new features, report bugs, and stay in the loop whenever a new update is available. 

## Setting up the bot (Read this before trying to use!):

# How to setup
Note: This instruction set is just a copy paste from marie, note that [TG BOT SUPPORT](https://t.me/TGBOTSUPPORT) aims to handle support for Phoenix and now how to setup your own fork, if you find this bit confusing/tough to understand then we recommend you ask a dev, kindly avoid asking how to setup the bot instance in the support chat, it aims to help our own instance of the bot. 

## Setting up the bot (Read this before trying to use!):
Please make sure to use python 3.6, as I cannot guarantee everything will work as expected on older python versions!
This is because markdown parsing is done by iterating through a dict, which are ordered by default in 3.6.

#Phoenix BOT
Hello, we are helping fork/clone on this project if you want to create clone of phoenix.

## Credits

Most of the credits goes to My Most Modules Helper [Goku](https://t.me/FaucetMaker) Have a donate if you like his work.
`Donate :-TRON :`

# Base Code
[MrHonekawa](https://github.com/mrhonekawa)/ [Edwin McCoy](https://t.me/mccoyeddy)

# Create Fork Of This Repo. (How To Do That)
`If Smartphone`
![Phoenix](https://telegra.ph/file/e70a9d65fa3afdda1df88.jpg)

Tap on button written as `Fork`.
It will take about few seconds to do that.
All Done; Congrats You Forked This Repo.

#Have Base Editing You Want in Code.

Just don't remove some codes; Don't change all the code just change `__init__.py` and `__main__.py`.

# Help on Funcs.

copy sample_config.ini and make a config.ini, satisfy the values in it.


 - `TOKEN`: Your bot token, as a string.
 - `OWNER_ID`: An integer of consisting of your owner ID
 - `OWNER_USERNAME`: Your username

 - `DATABASE_URL`: Your database URL
 - `MESSAGE_DUMP`: optional: a chat where your replied saved messages are stored, to stop people deleting their old 
 - `LOAD`: Space separated list of modules you would like to load
 - `NO_LOAD`: Space separated list of modules you would like NOT to load
 - `WEBHOOK`: Setting this to ANYTHING will enable webhooks when in env mode
 messages
 - `URL`: The URL your webhook should connect to (only needed for webhook mode)

 - `SUDO_USERS`: A space separated list of user_ids which should be considered sudo users
 - `SUPPORT_USERS`: A space separated list of user_ids which should be considered support users (can gban/ungban,
 nothing else)
 - `WHITELIST_USERS`: A space separated list of user_ids which should be considered whitelisted - they can't be banned.
 - `DONATION_LINK`: Optional: link where you would like to receive donations.
 - `CERT_PATH`: Path to your webhook certificate
 - `PORT`: Port to use for your webhooks
 - `DEL_CMDS`: Whether to delete commands from users which don't have rights to use that command
 - `STRICT_GBAN`: Enforce gbans across new groups as well as old groups. When a gbanned user talks, he will be banned.
 - `WORKERS`: Number of threads to use. 8 is the recommended (and default) amount, but your experience may vary.
 __Note__ that going crazy with more threads wont necessarily speed up your bot, given the large amount of sql data 
 accesses, and the way python asynchronous calls work.
 - `BAN_STICKER`: Which sticker to use when banning people.
 - `ALLOW_EXCL`: Whether to allow using exclamation marks ! for commands as well as /.

  ### Python dependencies

Install the necessary python dependencies by moving to the project directory and running:

`pip3 install -r requirements.txt`.

This will install all necessary python packages.

  ### Database

If you wish to use a database-dependent module (eg: locks, notes, userinfo, users, filters, welcomes),
you'll need to have a database installed on your system. I use postgres, so I recommend using it for optimal compatibility.

In the case of postgres, this is how you would set up a the database on a debian/ubuntu system. Other distributions may vary.

- install postgresql:

`sudo apt-get update && sudo apt-get install postgresql`

- change to the postgres user:

`sudo su - postgres`

- create a new database user (change YOUR_USER appropriately):

`createuser -P -s -e YOUR_USER`

This will be followed by you needing to input your password.

- create a new database table:

`createdb -O YOUR_USER YOUR_DB_NAME`

Change YOUR_USER and YOUR_DB_NAME appropriately.

- finally:

`psql YOUR_DB_NAME -h YOUR_HOST YOUR_USER`

This will allow you to connect to your database via your terminal.
By default, YOUR_HOST should be 0.0.0.0:5432.

You should now be able to build your database URI. This will be:

`sqldbtype://username:pw@hostname:port/db_name`

Replace sqldbtype with whichever db youre using (eg postgres, mysql, sqllite, etc)
repeat for your username, password, hostname (localhost?), port (5432?), and db name.

  ## Modules
   ### Setting load order.

The module load order can be changed via the `LOAD` and `NO_LOAD` configuration settings.
These should both represent lists.

If `LOAD` is an empty list, all modules in `modules/` will be selected for loading by default.

If `NO_LOAD` is not present, or is an empty list, all modules selected for loading will be loaded.

If a module is in both `LOAD` and `NO_LOAD`, the module will not be loaded - `NO_LOAD` takes priority.

  ### Creating your own modules.

Creating a module has been simplified as much as possible - but do not hesitate to suggest further simplification.

All that is needed is that your .py file be in the modules folder.

To add commands, make sure to import the dispatcher via

`from Phoenix import dispatcher`.

You can then add commands using the usual

`dispatcher.add_handler()`.
