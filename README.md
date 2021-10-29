# Many Worlds: the future of data collaboration

Collaboration requires having a shared *view* of the world. However,
it doesn't require that we share absolutely *everything*. Coming to a
shared concept of the state of something is what data collaboration is
all about.

To do this, you need a bit of exploration as to where your assumptions
line up with those of others. In order to collaborate you need ways to
minimize the stomping-on of toes. Collaboration is therefore a bit of
a dance.

*Git* really stands out as a tool for data collaboration on one of the
most complex types of data we have: Code. And the way we do this
collaboration is very different from the way we collaborate with one
of the other extremely widespread data collabration tools, the
database.

Now there are various kinds of databases, various replication
technologies, some very sophisticated and various levels of
[isolation](https://en.wikipedia.org/wiki/Isolation_(database_systems))
given which change the way we collaborate.

## The Many Worlds Database

The concept of isolation stems from the notion that databases should
have *one* world. Our transactions exist to construct *movement* in
this one world. This is really convenient when transactional commits
happen with reads and writes that are scheduled relatively close to
eachother and where scaling horizontally is not an issue. It works so
well that databases working on this model are absolutely pervasive in
our computer architectures.

Each database transaction is either a query, or a state transition.

* 

The pains of practice have forced relaxation

Even the way we think of [eventual consistency]()

Git is designed to tract changes to sets of files to facilitate
collaborative work among programmers. Many revision control systems
preceeded git, but none has been transformative of collaboration.

Why is this?

It's because git is a system for dealing with multiple worlds, 

Whether the authors of the software knew it or not

In Git you have a local repository, but you may also have remotes,
possibly many remotes.

Within your 
