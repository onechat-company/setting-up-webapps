# Setting up your own custom webapp

The following will be 2 different guides to creating and setting up webapps. The quick steps are for people who are experienced with networking and/or cloudflare. 

The in-depth steps are for those that are not familiar with networking, cloudflare or how any of that stuff works. 

## Quick Steps
- Register a domain for your business
- Create a Cloudflare account
- Add your domain to Cloudflare
- On the one chat dashboard, update your node's domain to what you'd like it to be;
	- (e.g. example.com or subdomain.example.com)
- On Cloudflare, add a new DNS query for the webapps
	- For a domain `type=CNAME name=@ target=webapp-one-chat-co.pages.dev proxy_status=true`
	- For a subdomain `type=CNAME name=subdomain target=webapp-one-chat-co.pages.dev proxy_status=true`
- On telegram, update your bot to use the domain/subdomain you created. You do that by speaking to `@BotFather`.
- Congrats you're done!

**Some things to note;**
- If you'd like to have your own business landing page, I highly recommend that you use a subdomain for the webapps.
- If you'd like a landing page made, I can do it as freelance for somewhere in the 1-10k range (depending on what you need, complexity ...etc)

## In-depth Steps

Glad to see you're interesting in using the webapps for your business. To be honest, this system is super badass and will only help you maintain and bring new customers over. Allowing people who refuse to use platforms like telegram use the website to message your workers. 

Currently though, only signing in with telegram is supported. In my next major update I will be adding discord, and a normal email/password sign in. All your customers currently use telegram, so it made sense to roll it out with telegram as the core functionality. 

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
``
### 6. That's it!

It's important to note that sometimes it can take some time for your domain to actually work with webapps. If it takes more then like 30 minutes, just shoot me a message and ill refresh it on my side.

If you're interested in running a landing page for your business, I don't mind taking it up as freelance. My pricing is typically between 1 - 10K depending on complexity and what you're wanting.

If you have any other questions or concerns please let me know!
