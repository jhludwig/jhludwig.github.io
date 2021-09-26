---
title: "Weekend experiment -- Amazon Codestar"
date: "2017-05-07"
---

Created a site using [Codestar](https://aws.amazon.com/codestar). It was pretty easy (the ssh setup instructions are the trickiest thing, they are not perfectly clear). And I like that the resultant site embraces AWS cloud services. But in its drive to easy dev, codestar masks what is going on under the covers, and I am left with a site that I don't really know how to modify and extend because I don't understand what has happened beneath me. I doubt I will use it much.

UPDATE: If you think of codestar as just a way to seed a project, it is kind of useful. it would have taken me a while to correctly configure IAM, CodeCommit, CodePipeline, CodeBuild, CloudFormation, and Lambda. A tool to seed a project with all this correctly set up is useful. I wish that the tool would emit a script to let me idempotently recreate the project from scratch including all IAM settings.
