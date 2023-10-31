# simple-deploy

There is a shortage of perfect ways to deploy software.

Hopefully this makes it a little bit easier.

## git-worktrees

Scenario: You want to deploy a web site to a web server. You also want
to be able to test on this website without clobbering your live site by
accident. Also you know git.

So you decide on git branches.

Now you need a way to turn git branches into directories on the server so
your apache or nginx instance can serve them.

So you write a script (this one) that maintains a bare git checkout and also
a set of git worktrees to match what your remote has. Now you just need to
run it every 1-60 minutes to sync your remote with the server.

Running a task every few minutes is a solved problem on Linux in so many
ways, so with this script already written and available, you can get going
much faster.
