---
title: Sustainable Web Dev
layout: post
date: 2021-7-6
categories: tech webdev climate environment
excerpt: Every website you visit has a carbon footprint. Google, Youtube, and yes, your hackathon project. The data centers and servers composing the Internet consume a vast amount of electricity and put out 3.7% of global carbon emissions, and this number is expected to double by 2025. With this in mind, how can we, as developers, ensure that our projects are as eco-friendly as they can be?
---

# SUSTAINABLE WEB DEVELOPMENT

Right now, you might be working remotely. You might be studying for your online classes or opening Zoom for a club meeting, rather than starting up the car. You’ve likely heard that at the start of quarantine, the CO2 emissions caused by transportation started to decrease, but how much carbon dioxide are you putting out as you drive, so to speak, through the Internet?  

Every website you visit has a carbon footprint. Google, Youtube, and yes, your hackathon project. The data centers and servers composing the Internet consume a vast amount of electricity and put out 3.7% of global carbon emissions, and this number is expected to double by 2025. With this in mind, how can we, as developers, ensure that our projects are as eco-friendly as they can be?  

<img src="/images/datacenters.jpg" alt="An aisle of servers in a data center.">
<center><i>Photo courtesy of pexels.com</i></center>  

# HOSTING

Let’s start with hosting. A web host is a service that makes your web application accessible to Internet users around the world, whether you are building your site from scratch or software like Wix or Wordpress. Green hosts power their data centers with renewable energy. The Green Web foundation provides a list of these green hosts here. Google and Amazon have switched to green hosting, meaning that if you deploy your app using their services (or any service using their services), your site will be hosted green.  

So, which hosts should you pick? That depends on how you are building your site.  

## If you are building your site using a web development engine…  

**Wix, Google Sites, and Blogspot** all run on Google Cloud, meaning that sites built on these platforms are hosted green. **Shopify,** an e-commerce service, recently migrated towards using Google Cloud after previously using AWS, both of which are green hosts. These four services cover a wide range of services—blogging, selling products, simply displaying information—allowing you to build websites for any purpose.  

If you use **WordPress,** your site will not automatically be hosted green. To transition your WordPress site to a green host, you may have to pay for an external service whereas Wix, Google Sites, and Blogspot allow you to publish sites for free.  

Unfortunately, **Weebly and Squarespace** are not reported to be hosting green.  


## If you are building your site from scratch…   

If you’re coding the site on your own, you’ll want to deploy your site to a web host to make it accessible by anyone on the Internet. How you decide to host depends on what languages and frameworks you’re using, and whether or not your site is static or dynamic.   

What does that mean? Static sites consist of “pre-built” files that display the same content for everyone. These sites are typically coded simply in HTML, CSS, and JS or using frameworks such as **React.js** and **Jekyll**. Dynamic sites, on the other hand, load content from a database to generate the site’s pages as they are requested. If you’re using a server-side framework such as **Node.js**, **Django**, or **Ruby on Rails**, you’re building a dynamic site.  

Here are some possibilities for hosting, listed in order of how easy they’ve been to use in my experience.  

- **[repl.it (free)](https://repl.it/){:target="_blank"}** is an incredibly beginner-friendly platform that uses a built-in IDE. It’s great for collaborative projects and supports a vast range of languages and frameworks. Their servers run on Google Cloud and AWS. I’d recommend this platform to test static web projects, though repl does support some server-side frameworks to a more limited extent (you’ll likely have to use an external database). Check out what languages they support here.  

- **[Firebase Web Hosting (free)](https://firebase.google.com/){:target="_blank"}** is a Google service great for deploying static sites. You can set up and deploy a web project on Firebase straight from your terminal, or use its online console. Unfortunately, Firebase doesn’t support dynamic sites—you won’t be able to deploy your Django project here.  

- **[Heroku (free, with paid features)](https://herokuapp.com/){:target="_blank"}** runs on AWS and supports both static and dynamic websites, built in any of the languages listed here. In my experience, it’s been much easier to deploy projects to Heroku than it has been using DigitalOcean and AWS. Its free tier is great for hobby projects and temporary hosting, though if you’re building a dynamic site, you’ll need to pay to have your project hosted continuously. Heroku’s file system is not persistent, meaning that if your project involves uploading media, you’ll have to use an external service to store this content.  

- **[DigitalOcean (at certain locations, paid)](https://www.digitalocean.com/){:target="_blank"}** offers a variety of cloud services such as databases, storage, and droplets to deploy your applications. It uses renewable energy at five of its data centers as of January 2020: NYC1, LON1, AMS2, AMS3, and SGP1. If you choose to deploy using DigitalOcean, your site will be hosted green if you base your droplet at these centers.  

- **[Amazon Web Services (paid)](https://aws.amazon.com/){:target="_blank"}** is working towards becoming 100% renewable by 2025, and passed 50% in 2018. They offer a vast range of services to support any of your web development needs (though I’ve only played around in AWS once, so its position as last on my list might not mean much!)  

Many of these hosts will allow you to choose a data location. Deploying your project to a data center close to your target audience will reduce the amount of processing power necessary to send data to your clients’ computers. If you’re building a site for your local community and you’re based in the East coast, pick New York City instead of San Francisco. If you expect most of your users to be Americans, choose a service location in the states rather than in Europe.  

<img src="/images/digitalocean.jpg" alt="Screenshot of DigitalOcean's UI with cards listing data center region. The developer can select which region they wish to host their project in.">
<center><i>DigitalOcean allows you to select a datacenter region when you create a droplet.</i></center>    
  
  
Some other common hosts, such as Github Pages and glitch.com, have not yet confirmed that they are running on sustainable energy or working towards it. Until they release more information, consider using one of the above services as an alternative.  

You can check if a site is hosted sustainably on [The Green Web Foundation's online database.](https://www.thegreenwebfoundation.org/){:target="_blank"}   

# CONTENT

Selecting a sustainable host isn’t the only way to make your site more eco-friendly—the content on your site plays a large role in how much processing power your site uses to access. Take a look at what kind of content you have on your site—each element has its own carbon footprint.  

Media files—images, videos, audio files, GIFs, and so on—take more processing power to load because of their filesize. Here are some tips on how to reduce their footprint:  

- If you’re using PNG and JPG images, replace with a **vector graphic** if possible—SVGs are much lighter than bitmap file formats. You can find SVG icons for nearly anything at [Icons8](https://icons8.com/){:target="_blank"}.  

- Similarly, if you’re using a video where you can use a **CSS animation**, opt for the animation instead! (Not sure how to animate using CSS? You can play around on [Animista](https://animista.net/){:target="_blank"} to build customized animations and generate the CSS code automatically.)  

- **Compress and resize your files.** Use compressed file formats such as JPGs instead of PNGs if the transparency of your image does not matter. Instead of relying on CSS to resize images, load them at the correct size. You don’t need a 2000x2000 image at 300dpi for your favicon!  

- Overall, **be mindful of where you decide to include media files.** Think about whether an image or a video is absolutely necessary to communicate your message and how much it really contributes to the UI/UX.  

- **Fonts**—font files are particularly heavy when you’re loading custom fonts rather than using default system fonts. One font file can add as much as 250KB—and using various weights such as bold and thin variations will throw another file on top of the package. Use the default system fonts wherever you can—often, these standard fonts make a more readable and accessible UI, anyways.  

**JavaScript** also increases your site’s carbon footprint. Scripts increase the amount of processing required to load your site, so if you are using JavaScript to aid with a frontend functionality, see if you can create the same effect with CSS. JavaScript is difficult to avoid for many web projects, yes—but make sure your code is clean and your algorithms are efficient to reduce redundancy or unnecessary processing.  

**Frameworks** such as Bootstrap and UIKit may make styling your page much easier, but usually aren’t necessary for small sites. Don't kill a fly with a flamethrower. Instead of loading an entire framework into your project, try writing the CSS yourself. It’ll take a little extra time, but will save a lot of processing power.  

Finally, dynamic sites use a lot more processing power than static sites do—and are more expensive to host! Save your own resources and the planet’s by **using a static site wherever possible**—if you want to display the same content for everybody, there’s no need to render pages from a database. Jekyll is a static alternative to Django—both frameworks allow you to render web pages from templates so you won’t have to copy and paste code for each page.  

<img src="/images/websitecarbon.jpg" alt="Screenshot of Website Carbon's analysis of a website. It estimates that this site is cleaner than 91% of sites tested, produces 0.11 grams of CO2 per visit, and is running on sustainable energy.">  
<center><i><a href="https://www.websitecarbon.com/" target="_blank">Website Carbon</a> estimates your website’s carbon footprint.</i></center>

# WHAT NOW?

If you’re like me, you’d now be clicking through the files of your code project, stressing over all the ways you now realize it contributes carbon emissions to our world. (Actually, you’re probably not doing this, which is all well and good. Please don’t stress.)  

As programmers, it’s important for us to keep in mind the ethical implications of our projects—and that includes their environmental impact. After I learned about the carbon footprint of web development, I challenged myself to revisit old projects and make small (yet heavy) changes—switching their web hosts, compressing images. The site websitecarbon.com provided a way to quantify my changes—this tool estimates your website’s carbon footprint based on its content and its hosting plan.  

But, as individual programmers, the carbon footprints of our personal projects are nothing in comparison to that of big tech. Aside from working on our own projects and whittling down on their carbon emissions, we can also make an impact by spreading the word. So talk to your coder friends. Sign petitions. Add a Website Carbon badge to your project to make your unsuspecting users grow curious about the cause.   

(Fun fact—seeing this badge on another programmer’s personal site drove me into a rabbit-hole of researching the environmental impacts of computing, so you have this badge to thank for the article you’re reading right now!)  

The carbon emissions of the Internet will only grow. In the age of social distancing, it’s especially crucial for the tech industry to design with awareness of their impact on our planet and its people. So keep your curiosity with you as you build your future projects, and check out some of the links below as starting points for your research. Read, learn, and share so that one day we may build ourselves a more sustainable cyberspace.  


# RESOURCES:
- [https://sustainablewebdesign.org](https://sustainablewebdesign.org){:target="_blank"}
- [https://www.websitecarbon.com/](https://www.websitecarbon.com/){:target="_blank"}
- [https://www.thegreenwebfoundation.org/](https://www.thegreenwebfoundation.org/){:target="_blank"}
- [https://www.wholegraindigital.com/blog/website-energy-efficiency/](https://www.wholegraindigital.com/blog/website-energy-efficiency/){:target="_blank"}  




  
  