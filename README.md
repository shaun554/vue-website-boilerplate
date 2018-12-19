# Vue Website Boilerplate

![nuxtjs-website-boilerplate](https://cosmic-s3.imgix.net/f761b6c0-31c3-11e8-b70e-833ed2e4b04d-nuxtjs-cosmicjs.jpg)
A website template that satisfies some common website requirements including dynamic pages, blog articles, author management, SEO ability, contact form and website search. Built using Vue and Nuxt.js. Contributions welcome!

## Demo
[Click here to view the demo](https://cosmicjs.com/apps/nuxtjs-website-boilerplate)

> [Read how this app was built](https://cosmicjs.com/articles/nuxtjs-website-boilerplate-jezdxaxb)

## Features
1. Fully responsive down to mobile w/ [Bootstrap](http://getbootstrap.com) frontend<br />
2. SEO ready<br />
3. A contact form that sends an email to your email(s) of choice and to [Cosmic JS](https://cosmicjs.com) for easy reference<br />
4. Full-site search functionality<br />
5. All content is easily managed in [Cosmic JS](https://cosmicjs.com) including pages, blog and contact info.

Sign up for [Cosmic JS](https://cosmicjs.com) to install the demo content and deploy this website.

## Getting Started

```bash
git clone https://github.com/cosmicjs/vue-website-boilerplate
cd vue-website-boilerplate
npm install

# Run in development and serve at localhost:3000
npm run dev

# build for production
npm run build

# Run in production and serve at localhost:3000
COSMIC_BUCKET=your-bucket-slug npm start
```
Import the `bucket.json` file into your Cosmic JS Bucket.  To do this go to Your Bucket > Settings > Import / Export Data.

<img src="https://cosmic-s3.imgix.net/44f0d590-0303-11e9-b4bb-b3fa3d766bf7-sendgrid.gif?w=1300" width="700" />

## Contact form setup
Install and deploy the SendGrid Email Function.

<img src="https://cosmic-s3.imgix.net/a07738c0-00d6-11e9-95fe-59d8fdd00c64-sendgrid-email.png?w=1500" width="700" />

The contact form on the contact page uses the [SendGrid Email Function](https://github.com/cosmicjs/send-email-function) to send emails. To deploy your email function go to Your Bucket > Settings > Functions. Install and deploy the SendGrid Function. You will need an account with [SendGrid](https://sendgrid.com/) to add your SendGrid API key.

### Add the SendGrid Function Endpoint

#### in development
Go to `config/index.js` and edit `SENDGRID_FUNCTION_ENDPOINT` to manually add the URL for testing.

#### in production
If you are using the Web Hosting option that's included with every Bucket:
1. Go to Your Bucket > Settings > Web Hosting
2. Deploy your Website
3. Click 'Set Environment Variables' tab and add the SendGrid Function endpoint:

Key | Value
--- | ---
| SENDGRID_FUNCTION_ENDPOINT     | https://your-lambda-endpoint.amazonaws.com/dev/send-email
