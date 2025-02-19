About this Repo
======

This is the Git repo of the official Docker image for [Odoo](https://registry.hub.docker.com/_/odoo/). See the Hub page for the full readme on how to use the Docker image and for information regarding contributing and issues.

The full readme is generated over in [docker-library/docs](https://github.com/docker-library/docs), specifically in [docker-library/docs/odoo](https://github.com/docker-library/docs/tree/master/odoo).

# Changes

Mostly not depending on a `.deb ` hosteed by them but our own

# Addition
We want odoo.deb to be inside the respective branch so that we can tell the dockerfile to copy the deb from within.

In order to generate this .deb you:
- Go to some other directory, say, `~/tmp`
- Then `git clone github.com/ottersome/odoo`
- Then, ensure all dependencies within `requirements.txt` are installed in your local/global python
- (Activate your environment if need be)
- Finally, you run `python setup/package.py --build-deb --no-remove`
- This will generate a build directory outside `~/tmp/odoo`
- Then you copy the `.*.deb` file within inside this repos branch of choice. 
- Then you build the image.
