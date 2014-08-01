## Introduction


### How to use the Drupal QA Checklist

The following will help in your use of the QA Checklist.
Information

This module was written for Drupal site builders, developers, and System administrators or anyone else in charge of launching a Drupal site. The tasks within represent a comprehensive list of things to review and tasks to perform before going live. If you need help with Drupal SEO best practices, the search engines' latest changes, your brand's target audience, or strategic marketing objectives, consider using a Drupal development shop consultant like WebOzy or others listed HERE.

### A bit about checklists

Each time you open the QAChecklist, it will look to see if any tasks have already been completed. For example, if you've already turned on clean URLs then that item will be checked. You still need to click "Save" to time and date stamp the automatically-checked items.

The tasks here are designed to be done sequentially, from top to bottom.

### Some notes

- Save Button: Be sure to click the save button after you check off each item. This will create a time and date stamp so that you can easily see when each task was completed.

- Help: Some items have "More info" links. These will take you to appropriate documentation pages where you can read more about a module or important concept.

- “Configure” may also mean “Install and configure”. At WebOzy we make frequent use of distros and server images. This means that the software is already installed, but still needs to be configured uniquely for each client.


- “Review” means to check over, the usual settings may be fine
    - **define**:*review* - to examine or assess (something) formally with the possibility or intention of instituting change if necessary. 


### Don’t do it all

Not every task in this list needs to, or even should, be done. Some of this will rely on your web host or PAAS provider. Using a Drupal-optimized provider such as Pantheon means that much of this list is already completed. Sit back and enjoy some iced tea. For standard web hosts, you may want to ask about the availability of certain points.

### Credits

The Drupal QA Checklist was created by Nicholas Garofalo (Eidolon Night), the CTO of WebOzy, Inc. and other staff members. Development was paid for exclusively by Volacci. Special thanks to Travis Carden who created the Checklist API and ported the 7.x-1.x branch. 

## Deployment

- Deploy code to live server
    - This checklist is meant to be performed on your live environment
Other checklists

## Other checklists

These are other checklists that would be good to complete.

- Security Review
    - Check the site for common Drupal security risks.

- SEO Checklist
    - Add some modules to help with SEO best practices.

- Site Audit
    - Drupal static site analysis platform that generates reports with actionable best practice recommendations.

- Performance and scalability checklist
    - Drupal static site analysis platform that generates reports with actionable best practice recommendations.

## Backups

- Install Backup and Migrate
    - This will help with your database backups if your host/PAAS doesn't do it for you.
    - PROJECT LINK

- Install Backup and Migrate Files
    - This addon helps backs up for files if your host/PAAS doesn't do it for you.
    - PROJECT LINK

- Configure Backup and Migrate settings
    - DESCRIPTION
    - PROJECT LINK

- Configure server-side backups
    - Using your hosts server-side backups ensures that you also save server configuration

## Maintenance

- Install DB Maintenance
    - DESCRIPTION
    - PROJECT LINK

- Run DB Maintenance
    - Module info... 

## Linux

- Review OS swappiness value
    - Check swappiness value to avoid the hard disks
Web server

- Review web server configuration
               Review Apache/Nginx configuration: max clients, timeouts, etc.
- Review configured vhosts 
    - Check for the proper vhosts for your site and any overrides that may be in those files.


   * Additional resources
   * 
      * Apache performance tuning http://httpd.apache.org/docs/current/misc/perf-tuning.html

## Database

- Review database configuration
    - Check cache sizes, default table type, etc.

- Review table storage engines
    - Recommended: innodb


   * Additional resources
   * 
      * High performance MySQL http://www.highperfmysql.com/


## Memcached

- Review memcached configuration
    - Check cache sizes, default table type, etc.

- Install memcached PHP extension
    - Recommended: innodb

- Install Memcache API and Integration module
    - DESCRIPTION
    - PROJECT LINK


   * Additional resources
   * 
      * High performance MySQL http://www.highperfmysql.com/

## PHP

- Review PHP configuration
    - Review PHP configuration: max execution, file uploads, etc.

- Review loaded PHP extensions
    - Status page link...

- [Optional] Install PHP opcode cache
    - Options; APC, eAccelerator, Xcache or OPcache (built into PHP 5.5)

- [Optional] Configure PHP opcode cache
    - Options; APC, eAccelerator, Xcache or OPcache (built into PHP 5.5) 

## Reverse proxy

- Install or setup reverse proxy cache
    - Recommended: Varnish or Nginx

- Configure reverse proxy cache
    - Recommended: Varnish or Nginx 

- Configure settings.php with reverse proxy IPs
    - Needs handbook page...

- Make sure cache control modules are configured and connected
    - DESCRIPTION
    - PROJECT LINK

- CDN (optional)

- Setup Content Delivery Network (CDN)
    - DESCRIPTION 

- Configure CDN
    - DESCRIPTION

## Drupal optimizations

- Review performance settings

- Review Views cache settings

- Install Elysia cron
    - DESCRIPTION
    - PROJECT LINK

- Configure Elysia cron
    - DESCRIPTION   

## User management

- Set administrator role
    - DESCRIPTION

- Review user registration settings
    - DESCRIPTION

- Review email settings
    - DESCRIPTION

- Install filter permissions module
    - DESCRIPTION

- Read managing…
    - DESCRIPTION

- Review and revise user permissions
    - DESCRIPTION
## Logs

- Check Drupal logs for issues
    - DESCRIPTION

- Check for core and module updates (update manager)
    - Make sure that Update Manager is enabled, run cron or sun the check manually, and then apply any necessary updates.
Cleanup

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

- Review site appearance as anonymous user
    - DESCRIPTION

- Review site appearance as authenticateduser
    - DESCRIPTION 

- Run pingdom tools check
    - DESCRIPTION  
Site launch
- Set up HTTP redirect in settings.php for www or non-www
    - DESCRIPTION

- Point DNS and/or CDN to new live server
    - DESCRIPTION 

- Set up cron job
    - DESCRIPTION

## Paid services (optional)

- I need help launching my site
    - Get in touch with [WebOzy](http://webozy.com/)

## Extras
Now that you've successfully launched your site, do something nice for yourself.

- Brew some fresh coffee

- Eat some bacon

- Do something nice for us
    - Link to WebOzy to thank them for this awesome module