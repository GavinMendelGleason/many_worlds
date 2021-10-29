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

In order to think about *data* and *change*, we're going to stray into
a universe of multiple worlds which was perhaps best conceptualised by
[Saul Kripke](https://en.wikipedia.org/wiki/Kripke_semantics) from
whom we will borrow liberally.

## Linear Worlds

The concept of isolation stems from the notion that databases should
have *one* world. Our transactions exist to construct *movement* in
this one world. This is really convenient when transactional commits
happen with reads and writes that are scheduled relatively close to
eachother and where scaling horizontally is not an issue. It works so
well that databases working on this model are absolutely pervasive in
our computer architectures.

Each database *query* tells us something about the state of the
current world. For instance, if we have a world `w` we can ask a
question `parent(X,Y)` where we get all `X` `Y` for which
`parent(X,Y)` is true.

```
w
⋆

w ⊢ parent(X,Y) ← {[X = jim,  Y = jane ], [X = jim,  Y = joe],
                   [X = kate, Y = elena], [X = kate, Y = tim]}
```

Here we have a world at which Jane and Joe are Jim's parents, and Tim
and Elena are still Kate's parent. That's sensible enough, but we may
need to update this world when Jim and Kate have children.

This requires a *state transition*. We will go from a world `w` to `w'`
via some state transition `σ`.

```
w   w'
⋆ → ⋆
  σ
```

Let's say sigma says that we are going to add a child Sarah of Jim and
Kate. We might write this as: `σ ̣≡ insert:parent(sarah,jim) ∧ insert:parent(sarah,kate)`.

Now we can get a different answer at `w` and `w'` for a question such as the following:

```
w ⊢ parent(sarah,Y) ← {}

w' ⊢ parent(sarah,Y) ← {[Y = jim], [Y = kate]}
```

Different worlds have different facts.

But these worlds are arranged in a *linear* fashion. This is how we
usually think of *our own* world. That is, we generally think of there
being a single time-line, and everything that happens is shared for
all participants. As those with a bit of experience with quantum
mechanics may know, this may very well *not* be true! However it is
*mostly* true at human scales.

## The Simulation

But when we try to simulate our understanding of the state of the
world we inevitably 

```
```

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
