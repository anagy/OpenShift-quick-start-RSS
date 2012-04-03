RSS feed for OpenShift quick-start applications
================================================

This simple application helps you to quickly setup an application which will 
generate an RSS feed about Red Hat OpenShift quick-start application pushed to
GitHub.

Hosting the application on OpenShift
-------------------------------------

Create an account at https://openshift.redhat.com if you don't have.

Create a Python 2.6 application

	rhc app create -a osquickstartrss -t python-2.6

Add this repository as upstream

	cd osquickstartrss
	git remote add upstream -m master git@github.com:anagy/OpenShift-quick-start-RSS.git
	git pull -s recursive -X theirs upstream master
	git push

Now you can tell your RSS reader the URL:

	http://osquickstartrss-$YOURDOMAIN.rhcloud.com

That's it.
