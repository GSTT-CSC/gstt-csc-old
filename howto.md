---
layout: howto
title: How-to
description: Instructions, SOPs and guides
---


<div class="card" style="width: 18rem;">
   <div class="card-body">
      <h5 class="card-title">Contents</h5>
      <ol>
      1. <a href="#update">Update this website</a>
      </ol>
   </div>
</div>



<hr>

## <a name=update></a>**Update this website**
`nb. if at any point something unexpected happens at any point STOP and ask for help!`
#### Do this first time, then skip  

1. Go to <https://github.com/GSTT-CSC/gstt-csc.github.io>
2. Hit the green `Code` button
3. Choose `Open with Github Desktop`
   > You'll be asked to download it if you don't have it
   
4. In Github Desktop (GHD), log in using your Github credentials and clone the repo locally

#### Usual process  

5. First create an issue for the change you wish to implement. You can do this by visiting github (link in the first point) and click on the tab `Issues` and click `New issue`
6. Describe the change you wish to implement in the comment box. Give it a sensible title that adequately represents the issue e.g. 'publish skills matrix'. Click on `Submit new issue`
7. The issue will then be reviewed by a team member. Once the issue is approved, create a new branch
8. To create a new branch in Github Desktop, click `current branch` button and then click `new branch`
9. Give it a short, sensible hyphen-separated name in the imperative e.g. update-team-page

      <div class="alert alert-info" role="alert">
        Your current branch should now show the name of your new branch
      </div>
   
10. Open a terminal and change directory (cd) to where your repo was cloned

11. Execute `bundle install`
   
    <div class="alert alert-danger" role="alert">
        For M1 Apple Macs instead do <code>arch -arch x86_64 bundle install</code>
    </div>


12. Execute `bundle exec jekyll serve`

     <div class="alert alert-danger" role="alert">
        For M1 Apple Macs instead do <code>arch -arch x86_64 bundle exec jekyll serve</code>
    </div>
   
      <div class="alert alert-success" role="alert">
        The website should be available locally on `http://localhost:4000` now
      </div>
   
13. Make changes to your code using your favourite editor/IDE (just use Pycharm)
    
      <div class="alert alert-info" role="alert">
        If you're updating AI projects or team page, then you might just need to edit the file in _data/
      </div>

14. Commit your code once you're happy with your changes using the template below
15. Publish your branch to github
16. On the Github website, go to `Pull requests` and click `New pull request`
17. Make sure the `base` branch is `main` and the `compare` branch is your published branch
18. Click `Create pull request`
19. This will allow your code to be reviewed by a team member and then merged into live website!

**Commit template** (read more here: <https://chris.beams.io/posts/git-commit/>> 
>      Summarize changes in around 50 characters or less
>     
>      More detailed explanatory text, if necessary. Wrap it to about 72
>      characters or so. In some contexts, the first line is treated as the
>      subject of the commit and the rest of the text as the body. The
>      blank line separating the summary from the body is critical (unless
>      you omit the body entirely); various tools like log, shortlog
>      and rebase can get confused if you run the two together.
>      
>      Explain the problem that this commit is solving. Focus on why you
>      are making this change as opposed to how (the code explains that).
>      Are there side effects or other unintuitive consequences of this
>      change? Here's the place to explain them.
>      
>      Further paragraphs come after blank lines.
>      
>       - Bullet points are okay, too
>      
>       - Typically a hyphen or asterisk is used for the bullet, preceded
>         by a single space, with blank lines in between, but conventions
>         vary here
>      
>      If you use an issue tracker, put references to them at the bottom,
>      like this:
>      
>      Resolves: #123 [1]
>      See also: #456 [2], #789 [3]
>      [1](http:// some url)
>      [2](http:// some url)
>      [3](http:// some url)

<hr>