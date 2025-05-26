# Setting up your own custom webapp

Hello and welcome to the webapp tutorial for One Chat. This is version 2 of the tutorial and new sections have been added for adding different authentication methods.

There will be a quick guide for those they are a bit more technologically inclined, and a full written tutorial for those that need to be walked through. 

## Quick Steps
- Register a domain for your business.
- Create a Cloudflare account.
- Add your domain to Cloudflare and update your domain so that it points to Cloudflare.
- On the One Chat dashboard, update your node's domain to what you'd like; 
	- (e.g. example.com or subdomain.example.com)
- On Cloudflare, add a new DNS query for the webapps
	- For a domain; `type=CNAME name=@ target=webapp-one-chat-co.pages.dev proxy_status=true`
	- For a subdomain; `type=CNAME name=subdomain target=webapp-one-chat-co.pages.dev proxy_status=true`
- On Telegram, update your bot to use the domain/subdomain you created. You can do that by speaking to `@BotFather`.
	- Make sure you update the domain and don't add a webhook. Adding a webhook will break bot functionality.
- Congrats you're done!

**Some things to note;**
- If you want to choose what authentication methods you allow on the webapps, you can modify this by editing your node on the One Chat dashboard.
	- To enable discord as an auth method, make sure you add the `client_secret` for your bot, and add the following redirect to the oauth2 page; `https://subdomain.example.com/node/auth/callback`. Obviously make sure you use the correct subdomain or domain.
- If you'd like to have your own business landing page, I highly recommend using the subdomain method and just directing your users to use the webapps. 
- If you'd like a landing page made, I can make them for you. My pricing is within the 1-10K range depending on what your needs are.

## In-depth Steps

I am very glad to see that you have interest in the webapps. Over the course of about a month I made my fully functional messaging/ticket app for you guys, of which I have been slowly updating and improving. Honestly, webapps are quite badass and will only help you maintain and bring new customers over to your business. Not all potential customers will want to use telegram or some social messaging app, having your own domain/website can come off much more professional, and with the bonus of allowing different auth methods, like email/pass or discord.

One last thing, the reason I made the webapps was because of telegrams change of focus towards questionable or interesting bots, channels and businesses using their platform. With AI being the centerfold of almost every tech company, it's possible that your channel, bots and other contents on telegram get taken down. The webapps are great at allowing customers to message off of telegram.

### 1. Getting started!

The first step to setting up webapps is with the domain. The domain will be the center of your business on the world wide web, and due to that, should aim at a catchy name, or something that reflects your business as a whole. The domain is what the customer will see in the address bar when navigating the webapps. 

**The following are examples of what domains look like;**
- one-chat.co
- onech.at
- facebook.com
- discord.com

**An example of what a subdomain can look like;**
- **revolt**.onech.at
- **webapp**.onech.at
- **messenger**.facebook.com
- **web**.telegram.org

If you can't think of a domain that you'd like, I recommend using the following service; https://domainr.com - Domainr can help you find any domain available with a word that you choose. 

![Pasted image 20250103162033](https://github.com/user-attachments/assets/e811972b-2964-4d88-9315-092c81b00a08)

### 2. Registering a domain

So you found your dream domain "burgersandfri.es". The next step is purchasing it. There are plenty of different services you could use; namecheap, godaddy, google, squarespace (the list goes on)...

I highly recommend using https://njal.la/ -- they ask for no personal information, and you can pay for your domain with cryptocurrency. Remember, when dealing with anything online, opsec (operational security), and privacy are the upmost importance. 

### 3. You've got the domain, what's next?

Once you have your domain purchased, your next step will be creating an account on https://cloudlare.com - Cloudflare is a DNS service, this basically tells infrastructure where your website is located so that people can actually see it. Cloudlfare also has tons of tools, many of which I utilize in my One Chat Development. 

Once your account has been created, you will need to add your domain to their service (you can select the free tier).

Cloudflare will give you two nameservers that will point your domain to their service, you update this from the registers DNS/NS tab. 

### 4. Updating your node

Go to the One Chat dashboard, and navigate to the [One Chat - Nodes](https://app.one-chat.co/nodes) page. Edit your businesses node, and add the domain (e.g. business.com or webapp.business.com).

### 5. Connecting the domain to the webapps

Go to cloudflare, and navigate to your domains DNS settings. We now want to point your domain or subdomain to our cloudflare pages. 

**To point a domain;**
`type=CNAME name=@ target=webapp-one-chat-co.pages.dev proxy_status=true`

**To point a subdomain;**
`type=CNAME name=subdomain target=webapp-one-chat-co.pages.dev proxy_status=true`

![image](https://github.com/user-attachments/assets/d0465d41-dff3-4b4f-815b-7cd0b3cd97ef)

### 6. Update your telegram bot

On telegram, contact `@BotFather` and make sure to add your domain/subdomain to your bot. Use the command `mybots` to get a list of any bots attached to your current account. Click on the bot you're wanting to use for authentication, then click on `Bot Settings`, `Domain` and send your domain. 

**Example;** `subdomain.example.com`

### 7. Adding discord as an authentication method

Version 1 of this tutorial stated that the only auth method allowed was Telegram, this has now changed. Email and password authentication is now supported, and discord authentication is now supported. 

To enable discord authentication, you first need to go to the [Discord Developers Dashboard](https://discord.com/developers/applications). Click on your discord bot you'd like to use for authentication and then navigate to the `OAuth2` page.

On the OAuth2 page you will need to add a redirect to your domain. That should look like the following; `https://subdomain.example.com/node/auth/callback` or `https://domain.com/node/auth/callback`. Then make sure to save your changes.

![image](https://github.com/user-attachments/assets/81e92596-4e6a-4be4-a696-bb16f819af15)

![image](https://github.com/user-attachments/assets/a3102030-0c1a-4765-b1a7-0f7780c4d723)

On that same OAuth2 page you will notice a section that says `Client Secret`, you will need to reset the secret and then add that to your [bot on the One Chat Dashboard]([One Chat - Bots](https://app.one-chat.co/bots).

![image](https://github.com/user-attachments/assets/e5375f86-ca72-44db-b234-6dcd5cf3ce9b)

Then make sure you edit the node, and add the discord, telegram and/or enable the email authentication. 

![image](https://github.com/user-attachments/assets/995d4c4c-df59-4005-a0ce-80fd19b67044)


### 8. That's it!

It's important to note that sometimes it can take some time for your domain to actually work with webapps. If it takes more then like 30 minutes, just shoot me a message and ill refresh it on my side.

If you're interested in running a landing page for your business, I don't mind taking it up as freelance. My pricing is typically between 1 - 10K depending on complexity and what you're wanting.

If you have any other questions or concerns please let me know!
