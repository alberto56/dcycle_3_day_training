---
layout: none
title: Test & CI training
---

Test & CI training
==================

Slides
------

Code: https://github.com/alberto56/dcycle\_3\_day\_training
Slideshow: http://alberto56.github.io/dcycle\_3\_day\_training/

Git repos
---------

Drupal 7: -
Drupal 8: -

Temporary Jenkins server
------------------------

This server has been set up temporarily for demo purposes and should not be considered secure.

Jenkins: http://x.x.x.x:8080
Jenkins username: admin
Jenkins password: -

SSH access: ssh root@x.x.x.x

(ask someone to put your ssh public key in root@x.x.x.x:~/.ssh/authorized_keys)

Please perform operations as the jenkins user to avoid permissions issues.

    sudo su -s /bin/bash jenkins

Environments
------------

All environments are publicly accessible via the web, and they are all on the same machine (not best practice, but OK for the demo)

- Jenkins environment
  http://-.dcycleproject.org
	x.x.x.x:/var/lib/jenkins/workspace/-
  Unstable
  What the jenkins server uses for testing

- Dev environment
	http://-.dcycleproject.org
	x.x.x.x:/var/lib/jenkins/www/d
  Stable (tests pass)
  Dummy and test content

- Preprod (or "staging") environment
	http://-.dcycleproject.org
	x.x.x.x:/var/lib/jenkins/www/pp
  Stable (tests pass)
  A clone of all real content

- Prod environment
	http://-.dcycleproject.org
	x.x.x.x:/var/lib/jenkins/www/pp
  Update has to be initiated by a human
  (unless we use continuous deployment)
