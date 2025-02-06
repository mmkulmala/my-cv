# my-cv
My resume in jsonresume format

[jsonresume](https://jsonresume.org)

## Instruction how I did my resume
I like to believe that sharing is caring, so I'll show you how I made my resume generation easy and free (always a bonus in these times ;) )

First goto jsonresume cli to have a client to your resume [jsonresume cli](https://github.com/jsonresume/resume-cli)

1. Simple just goto to any folder you want your resume, open shell and type:
```
npm install -g resume-cli
```

Voila! You got the resume-cli ready to create nice looking resumes! Next you need some themes to go with your resume ;)!

But before we jump there, you can test out resume-cli by running command from below in the shell:
```
resume -V
```
Output should be `3.0.8`

2. Now you need the jsonresume template, which can be found [here](https://jsonresume.org/schema), or you can do as I did and take your LinkedIn as a baseline ;). This can be done following [these instructions](https://jsonresume.org/getting-started) and installing Chrome addon to save your LinkedIn info as jsonresume. NOTICE that this addon is marked for deletion, so be quick if you plan to follow my footsteps.

If you just want to do it by. then all you need is the resume.json in some folde.

3. After the template, it's time to choose a theme for your resume by looking at the [jsonresume themes](https://jsonresume.org/themes) for some examples, but there are more than those available! 

This is how you install them (at least how I got them working..)

Do this in the same folder you have your resume.json:
```
npm install jsonresume-<choose-the-name-you-want>
```

You have to pick a name of theme to put in the `<choose-the-name-you-want>`  placeholder.

4. Now you can get your image to go with your resume if you like.

To get your github account id do [this](https://www.storylane.io/tutorials/how-to-find-github-id)

Now copy the id from last instruction link to `<YOUR_GITHUB_ACOUUNT_ID>` link below:
```
"image": "https://avatars.githubusercontent.com/u/<YOUR_GITHUB_ACOUUNT_ID>?v=4",
```

Then copy that into your resume.json, in place of `"image":` block in `resume.json`. That goes and gets your image from github and adds to your resume. Note that some themes are broken and image might not work, but I'll show how to test them out later on ;).

5. As all the preparations are done, we can finally got down to create some resumes!

All you need to do is type this into folder containing ´resume.json´:
```
resume serve --theme <CHOOSE_A_THEME>
```

In placeholder `<CHOOSE_A_THEME>` you put the theme you choose and you should see a new browser tab/window opening into pport 4000 and your resume. Easy, right?

But you most likely want your resume in pdf (classic format ;) ). Then you need to run this command where your `resume.json` is:
```
resume export <NAME-FOR-RESUME> --theme <NAME-OF-THEME>
```

Two placeholders:
* NAME-FOR-RESUME = the name of your resume to be saved plus `.pdf` to tell the format, example test-resume.pdf
* NAME-OF-THEME = the name of theme like kendall

If run the command, it tells you that it created your resume in the same folder as your resume.json. Go check it out and it should look just like the one you tested with `serve` command. 

And thats it! If you noticed something wrong, ping me and I'll update these instruction to match any findings!

Cheers and happu resuming ;)



