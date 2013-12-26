Saiku Analytics on OpenShift
======================

This git repository helps you get up and running quickly a Saiku Analytics installation
on OpenShift in a couple minutes with demo data (foodmart database). The backend database is MySQL and the database name is the 
same as your application name (using getenv('OPENSHIFT_APP_NAME')).  You can name
your application whatever you want.

Running on OpenShift
----------------------------

Create an account at http://openshift.redhat.com/ and install the client tools (run 'rhc setup' first)

Create a Tomcat 6 (JBoss EWS 1.0) application (you can call your application whatever you want)

    rhc app create saiku jbossews-1.0 mysql-5 --from-code=https://github.com/latinojoel/saiku-openshift-quickstart.git

That's it, you can now checkout your application at:

    http://saiku-$yournamespace.rhcloud.com
    
In the first execution the administrator credentials are admin/admin.

**Note:** Quickstart doesn't work on scalable mode because needs setup up the foodmart database manually.
