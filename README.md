# Textual overview of checklist

## Introduction

### How to use the Drupal QA Checklist

The following will help in your use of the QA Checklist.
Information

This module was written for Drupal site builders, developers, and System administrators or anyone else in charge of launching a Drupal site. The tasks within represent a comprehensive list of things to review and tasks to perform before going live. If you need help, or this list doesn't make any sense to you, we suggest hiring a Drupal development shop like [WebOzy](http://webozy.com/) or others listed in the [Marketplace](https://www.drupal.org/drupal-services).

### A bit about checklists

Each time you open the QAChecklist, it will look to see if any tasks have already been completed. You still need to click "Save" to time and date stamp the automatically-checked items.

The tasks here are designed to be done sequentially, from top to bottom.

### Don’t do it all

Not every task in this list needs to, or even should, be done. Some of this will rely on your web host or PAAS provider. Using a Drupal-optimized provider such as Pantheon means that much of this list is already completed. Sit back and enjoy some iced tea. For standard web hosts, you may want to ask about the availability of certain features.

### Credits

The Drupal QA Checklist was created by [Nicholas Garofalo (Eidolon Night)](https://www.drupal.org/user/191336), the CTO of WebOzy, Inc. and other staff members. Special thanks to [Travis Carden](https://www.drupal.org/user/236758) who created the [Checklist API](https://www.drupal.org/project/checklistapi) and ported the 7.x-1.x branch.

> #### Notes
>
> - Be sure to click the **save** button after you check off each item. This will create a time and date stamp so that you can easily see when each task was completed.
> - Some items have "More info" links. These will take you to appropriate documentation pages where you can read more about a module or important concept.
> - “Review” means to check over, the usual settings may be fine
>     - **define**:*review* - to examine or assess (something) formally with the possibility or intention of instituting change if necessary. 

## Deployment
Your first task! Gook luck!

- Deploy code to live server
    - This checklist is meant to be performed on your live environment.

## Other checklists (optional)
These are other checklists that would be good to complete.

- Security Review
    - Check the site for common Drupal security risks.
    - https://www.drupal.org/project/security_review
- SEO Checklist
    - Add some modules to help with SEO best practices.
    - PROJECT LINK
- Site Audit
    - Drupal static site analysis platform that generates reports with actionable best practice recommendations.
    - PROJECT LINK
- Performance and scalability checklist
    - A checklist of some performance and scalability best practices.
    - PROJECT LINK

## Backups
A good backup strategy prevents you from having a really bad day.

- Install Backup and Migrate
    - This will help with your database backups if your host/PAAS doesn't do it for you.
    - PROJECT LINK
- Install Backup and Migrate Files
    - This addon helps backs up for files if your host/PAAS doesn't do it for you.
    - PROJECT LINK
- Configure Backup and Migrate settings
    - Schedule these as frequently as you need, but remember that for large sites a scheduled backup can bring everything down.
    - PROJECT LINK
- Configure server-side backups
    - Using your hosts server-side backups ensures that you also save server configuration.

## Maintenance
You want to make sure that your site keeps performing well, these steps help you do just that.

- Install DB Maintenance
    - Keep your database clean and running smoothly. Note: You db server needs to be running a few days to get useful results.
    - PROJECT LINK
- Run DB Maintenance
    - CONFIGURE LINK

## Linux
Some changes to how your OS behaves can help with resource usage and ensure that you get the most out of your server.

- Review OS swappiness value
    - Check swappiness value to avoid swapping to the hard disks. Be careful and make sure that you have enough memory.
    - MORE INFO (NEEDS DOCUMENTATION)

## Web server
No matter which web server technology you use, the default settings simply won't do.

- Review web server configuration
    - Review Apache/Nginx configuration: max clients, timeouts, etc.
- Review configured vhosts 
    - Check for the proper vhosts for your site and any overrides that may be in those files.

> #### Additional resources
> Apache performance tuning: http://httpd.apache.org/docs/current/misc/perf-tuning.html
> Nginx performance tuning: http://www.slashroot.in/nginx-web-server-performance-tuning-how-to-do-it
> > OTHER HELPFUL STUFF


## Database
The database is Drupal's backend, so let's treat her well.

- Review database configuration
    - Check cache sizes, default table type, etc.
- Review table storage engines
    - Recommended: innodb
    - Info: DRUPAL DOCUMENTATION

> #### Additional resources
> High performance MySQL http://www.highperfmysql.com/


## Memcached (optional)
Memcached is a great cache option that is especially useful for sites with a high number of authenticated users.

- Review memcached configuration
    - Check cache sizes, default table type, etc.
- Install memcached PHP extension
    - SITE LINK
- Install Memcache API and Integration module
    - Integration between Drupal and Memcached
    - https://www.drupal.org/project/memcache
    - DOCUMENTATION LINK

## PHP
A few changes to your PHP config can provide major performance enhancements.

- Review PHP configuration
    - Review PHP configuration: max execution, file uploads, etc.
    - PHP INFO LINK
- Review loaded PHP extensions
    - PHP INFO LINK
- [Optional] Install PHP opcode cache
    - Options; APC, eAccelerator, Xcache or OPcache (built into PHP 5.5)
- [Optional] Configure PHP opcode cache
    - Options; APC, eAccelerator, Xcache or OPcache (built into PHP 5.5) 

## Reverse proxy (optional)
Reverse proxies cache your site's static content and can be configured to serve entire pages to anonymous user.

- Install a reverse proxy cache
    - Recommended: Varnish or Nginx
    - LINK FOR VARNISH
    - LINK FOR NGINX
- Configure reverse proxy cache
    - Recommended: Varnish or Nginx
    - LINK FOR VARNISH
    - LINK FOR NGINX
- Configure settings.php with reverse proxy IPs
    - HANDBOOK PAGE LINK
- Make sure cache control modules are configured and connected
    - DESCRIPTION
    - https://www.drupal.org/project/varnish
    - https://www.drupal.org/project/expire
- Check the status
    - https://www.drupal.org/project/reverse_proxy_check

## CDN (optional)
A CDN can decrease resource usage and give your site a major performance boost.

- Setup Content Delivery Network (CDN)
    - DESCRIPTION 
- Configure CDN
    - DESCRIPTION
- Install control module
    - https://www.drupal.org/project/cdn

> ####Additional resources
> Cloudflare https://www.cloudflare.com/
> https://www.drupal.org/project/cloudflare

## Drupal optimizations
Drupal has a few settings that enable caching.

- Review performance settings
    - PERFORMANCE PAGE LINK
- Review Views cache settings
- Install Elysia cron
    - Elysia Cron allows more advanced scheduling of your cron tasks.
    - https://www.drupal.org/project/elysia_cron
- Configure Elysia cron
    - Review your cron jobs and create some sane schedules.   

## User management
Users are your biggest threat. Let's review a few settings.

- Set administrator role
    - Since you'll probably be sharing admin access, you'll want a proper admin role.
    - USERS AND PERMISSIONS LINK
- Review user registration settings
    - Check the 
    - USER SETTINGS LINK
- Review email settings
    - Review the text and instructions of the welcome and verification emails.
    - USER SETTINGS LINK
- Install filter permissions module
    - 
    - DESCRIPTION
- Read managing…
    - DESCRIPTION
- Review and revise user permissions
    - DESCRIPTION

## Logs
Logs can be the first indicator for issues that will get much worse when you launch.

- Check Drupal logs for issues
    - Anything noticable? Review your logs for anything that stands out.
    - RECENT LOG ENTRY LINK
- Check for core and module updates (update manager)
    - Make sure that Update Manager is enabled, run cron or sun the check manually, and then apply any necessary updates.
    - UPDATE PAGE LINK

## Cleanup
The following tasks that cleanup our tools, settings, logs, etc. that are performance killers and/or security risks.

- Disable devel modules
    - Disabled for security and performance
- Disable Update Manager
    - Disabled for performance
- Disable Database Logging
    - Disabled for performance
- Set maintenance theme
    - DESCRIPTION
- Clean CSS files with CSS tidy
    - DESCRIPTION
- Disable PHP error message display
    - DESCRIPTION
- Change Drupal, MySQL, and SSH passowrds
    - DESCRIPTION
- Set up site emailing
    - Recommendaed: Mandrill module

## Front-end review
These tasks ensure that the end-user has a pleasurable experience on-site.

- Review site appearance as anonymous user
    - DESCRIPTION
- Review site appearance as authenticated user
    - DESCRIPTION 
- Run pingdom tools check
    - http://tools.pingdom.com/  
Site launch
- Set up HTTP redirect in settings.php for www or non-www
    - DESCRIPTION
- Point DNS and/or CDN to new live server
    - DESCRIPTION 
- Set up cron job
    - DESCRIPTION

## Paid services (optional)
Looking for something cool and have some money to spend?

- Throw out a lot of this list [get Pantheon](https://www.getpantheon.com/)
- I need help launching my site
    - Get in touch with [WebOzy](http://webozy.com/)

## Extras
Now that you've successfully launched your site, do something nice for yourself.

- Brew some fresh coffee
- Eat some bacon
- Do something nice for us
    - Link to WebOzy to thank them for this awesome module