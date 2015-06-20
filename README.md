# collectiveaccess
CollectiveAccess 1.4 on OpenShift

## CollectiveAccess
* [CollectiveAccess](http://www.collectiveaccess.org)
* [Download CollectiveAccess v1.4](https://github.com/collectiveaccess/providence/tree/release-1.4)
* [Installing Providence](http://docs.collectiveaccess.org/wiki/Installing_Providence)

## OpenShift
* Create a free [Red Hat Openshift account](https://openshift.redhat.com)
* [Getting started with OpenShift](https://openshift.redhat.com/app/getting_started)

## Installation
1. Login into [OpenShift](https://openshift.redhat.com)
2. Click Add Application
3. Select PHP-5.4
4. In Public URL, name your application (e.g. 'collectiveaccess')
5. In Source Code, type `git://github.com/perryrothjohnson/collectiveaccess.git`
6. Leave all other default options, click Create Application
7. Continue to the application overview page
8. Add MySQL cartridge to your application
8. Click 'see the list of cartridges you can add,' and add CRON cartridge to your application
9. Restart MySQL so server recognizes environmental variables in setup.php: Git clone respoitory, change value of `__CA_ADMIN_EMAIL__`, git add file, git commit, and git push
10. Setup [SSH keys for your application](https://developers.openshift.com/en/managing-remote-connection.html#keys). If necessary, [manually create and upload an SSH key](http://docs.openshift.com/online/user_guide/ssh_keys.html#tutorial-creating-and-uploading-ssh-keys). To upload an SSH key through the webapp, click Settings, add a new Public Key, and paste the contents of `~/.ssh/id_rsa.pub`.
11. In OpenShift, click Want to log in to your application? Copy the command below, and SSH into your application
12. Set permissions for `app/tmp` and `media` directories in CollectiveAccess:  
`$ cd app-root/runtime/repo/php/app`  
`$ mkdir tmp`  
`$ chmod 757 tmp`  
`$ cd ..`  
`$ chmod 757 media`
13. In a browser, go to [public URL]/install and start CollectiveAccess installation
14. Type in the administrator's email address, select the installation profile (e.g. California Science Center), and click Begin installation
