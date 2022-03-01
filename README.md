# rekt.news

## consistency guide

```
                   rekt → rekt

                   ...k → .000
                   ...m → Millionen
                   ...b → Milliarden
                 $35.3m → 35,3 Millionen US-Dollar

                 <date> → dd.mm.yyyy
                 <time> → hh:mm UTC
          <date>+<time> → am dd.mm.yyyy um hh:mm UTC

                    TVL → TVL
                    CEX → CEX
                    DEX → DEX
                   CeFi → CeFi
                   DeFi → DeFi

                    gas → das Gas
                   anon → der Anon
                 native → native
                   fork → der Fork
                   pool → der Pool
                   swap → der Swap
                  asset → das Asset
                  claim → der Claim
                  stake → der Stake
                  token → der Token
                  trade → der Trade
                  NFT   → das NFT
                 bridge → die Bridge
                 wallet → die Wallet
                airdrop → der Airdrop
               contract → der Contract
               treasury → die Treasury
              bagholder → der Bagholder
              community → die Community
              flashloan → der Flashloan
              front-end → das Front-End
              rug(pull) → der Rug(pull)
             governance → die Governance
            post-mortem → das Post-Mortem
      (cross-/on-)chian → die (cross-/on-)Chain

                   mint → minten
                wrapped → wrapped
```

## repositories

1. **[rektHQ](https://github.com/RektHQ/Resources)** (rekt repository)
2. **[rekt-de](https://github.com/ohyi/rekt.news)** (repository used here for translating)


## folder setup

~~~text
rekt-de
├── content_for_reference
├── done              # 4. process complete
├── user-a
│   ├── translating   # 1. user-a: translate article
│   ├── check         # 2. user-b: check article
│   └── ready         # 3. user-a: submit to rektHQ
└── user-b
    ├── translating
    ├── check
    └── ready
~~~


## translation process

### translate article (user-a)

~~~bash
cd rekt-de/<user-a>

git pull   # fetch from and merge with another repository or local branch
git mv ../content-for-reference/en/<article>.md translating/
git commit --message 'start translating <article>'
git push   # push commit to github server. ensures that 2nd translator doesn't translate same article.
~~~

edit the article in your favourite editor.

~~~bash
cd rekt-de/<user-a>

git commit --message 'completed about half of translation.' translating/<article>.md
git push   # push commit to github server
~~~

once you have completed translating the article, you move it to the _check_ directory.

~~~bash
cd rekt-de/<user-a>

git pull   # if it's been a while since your last pull
git mv translating/<article>.md /check/
git commit --message 'completed translation. ready for check.'
git push   # push commit to github server
~~~

let the other translator know that there is an article ready to be checked.

### check article (user-b)

~~~bash
cd rekt-de/<user-a>

git pull   # ensure you have the most recent version of the article

# check the newly translated article.
# correct it if necessary and transfer the article to the _ready_ directory:
git mv check/<article>.md /ready/
git commit --message 'fixed a couple of minor issues and is now ready for PR.'
git push   # push commit to github server
~~~

let the other translator know that the article is done.

### pull request (user-a)

as soon as an article has hit your _ready_ directory, the article can be submitted to rektHQ.

consult the guide provided by rekt translation team for comprehensive guide.

**tl;dr**

~~~bash
cd rektHQ

git fetch  # download objects and refs from another repository
git pull   # fetch from and merge with another repository or local branch

# create new branch that will be used to house the new article
git checkout -b trans/de/<article>
cp -a /path/to/rekt-de/<user-a>/ready/<article>.md content/de/

# add the article to the new branch
git add content/de/<article>.md

# commit changes to local copy of git
git commit --message 'commit de translation of <article>'

# push changes to rektHQ repository on the github server
git push origin trans/de/<article>
~~~

the output of the last git command will include a link to the pull request. you
can use the provided link or go to: https://github.com/RektHQ/Resources/pulls
to submit a pull request. make sure _base_ is set to **devolop** and complete
the provided _pull request template_.

once this is complete let the other translator know that you have committed the
article or let the translator team know. any translator can approve the article
since the article has already been checked by the second translator.

~~~bash
cd rekt-de

git pull   # if it's been a while since your last pull
git mv <user-a>/ready/<article>.md done
git commit --message '<article> has been submitted to rekt.'
git push   # push commit to github server
~~~

