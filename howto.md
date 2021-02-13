# **How-to**

## Update this website

### Do this first time, then skip
1. Go to <https://github.com/GSTT-CSC/gstt-csc.github.io>
2. Hit the green "Code" button
3. Choose "Open with Github Desktop"
   > You'll be asked to download it if you don't have it.
   
4. In Github Desktop (GHD), log in using your Github credentials and clone the repo locally

### Usual process
5. Check with Haris about the changes you would like to make first
6. In GHD, click current branch button and then click new branch
7. Give it a short, sensible hyphen-separated name in the imperative e.g. update-team-page
   >  Your current branch should now show the name of your new branch
8. Open a terminal and change directory (cd) to where your repo was cloned
9. Execute `bundle exec jekyll serve` 
   > the website should be available locally on `http://localhost:4000` now
   > 
10. Make changes to your code using your favourite editor/IDE (just use Pycharm)
   > See the changes update on your local website by refreshing `http://localhost:4000`
11. Commit and push your code once you're happy with your changes using the template below
12. 



`
      
      Summarize changes in around 50 characters or less
      
      More detailed explanatory text, if necessary. Wrap it to about 72
      characters or so. In some contexts, the first line is treated as the
      subject of the commit and the rest of the text as the body. The
      blank line separating the summary from the body is critical (unless
      you omit the body entirely); various tools like log, shortlog
      and rebase can get confused if you run the two together.
      
      Explain the problem that this commit is solving. Focus on why you
      are making this change as opposed to how (the code explains that).
      Are there side effects or other unintuitive consequences of this
      change? Here's the place to explain them.
      
      Further paragraphs come after blank lines.
      
       - Bullet points are okay, too
      
       - Typically a hyphen or asterisk is used for the bullet, preceded
         by a single space, with blank lines in between, but conventions
         vary here
      
      If you use an issue tracker, put references to them at the bottom,
      like this:
      
      Resolves: #123 [1]
      See also: #456 [2], #789 [3]
      [1](http:// some url)
      [2](http:// some url)
      [3](http:// some url)
`