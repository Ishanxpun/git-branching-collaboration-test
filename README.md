import React from 'react'

const git = () => {
return (

<div>

{/\* _to create new branch: _/}
-git branch branchname

{/\* _ to switch branch : _/}
-git checkout branchname

{/_ to rename branch: _/}
- git branch -M rename
  -git push -u origin main

{/_ when u rename master branch to main ,github web ma chai master rename hunna but there will be 2 branches main and master(default) _/}
{/_ change default to main and delete master _/}

{/\* _ to delete branch: _/}
-git branch -d branchname (branch delete garna xa vani next branch ma gayera balla delete garni. tei branch ma basera tei branch del hunnna)

{/_ to push branch remotely : git push garda branch haru push hudaina_/}
-git push -u origin branchname

{/\* _ merge branch: _/}
{/_ way 1. _/}
merge 2 branches: -git merge branchname/main (feature vanni branch ma basera main ma merge)
-to compare commit,brnaches,files :git diff branch name

           {/* way 2. */}
    	          pull req: -mero branch chai main sanga merge han vanera vanni request ani senior/owner accepts and remotely merge hunxa
    		                -GitHub ma merge vayo tara locally merge vaxaina vani pull command use garni
    		                -pull command is used fo fetch content from remote repo to local
                            {/* pull:fetch + merge */}

-git pull origin main
{/_ or we can do fecth and merge indiviually _/}
{/_ pull le direct remote bata fetch garera merge garxa but individual fech+headerlog+merge garda chai
fetch le locally ma lyauxa tara no change and we see git log header to see changes if we like then add git merge _/}
-git fecth
-git log HEAD..origin/main # see what changed
-git merge origin/main # brings changes into your branch
{/_ main branch ma xa vani tei mathi ko commad but feature branch ma xa vani git merge main garni ani mathi ko command i.e 1 line extra _/}

{/\* _merge conflict:two branch ma eutai thauma chanes garayo vanigit unable to resolve so we manually solve. _/}
eg:btn add in 1 branch and dropdown add in another then git confuse
-git merge main
conflict show garxa and k k lie add garxa tyo line hatauni .now button and dropdown same ma auda kun chahinxa tei rakhni

{/\* _undoing changes _/}
1:staged changes
-git reset filename
-git reset (for multi)

2:commit changes for 1 commit
-git reset HEAD~1

3:commit changhes for many commit
-git log // shows all commit history whith hash
-q // for quit

-git reset commitHashPaste
-git reset --hard commit hash // github ma matra haina vs code ma ni change hunxa

</div>
)
}

export default git
