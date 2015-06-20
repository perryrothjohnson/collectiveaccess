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
7. Add MySQL cartridge to your application
8. Add CRON cartridge to your application
9. Restart MySQL so server recognizes environmental variables in setup.php: Git clone respoitory, change value of `__CA_ADMIN_EMAIL__`, git add file, git commit, and git push.
10. In a browser, go to [public URL]/install and start CollectiveAccess installation
11. You can test now CollectiveAccess on OpenShift without any warranty. 
