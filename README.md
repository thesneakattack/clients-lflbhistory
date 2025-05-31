Pulling in submodules (child repos):
Initialize (if you haven’t already) and fetch every submodule:
git submodule update --init --recursive
To pull in the latest commits from each submodule’s default branch
git submodule update --remote --recursive

(Optional) Commit the updated submodule pointers in the parent
Whenever any submodule moves (because you pulled new commits), the parent sees it as “that submodule now points at a different commit.” If you want the parent to remember those updated pointers, do:
git add cms site exhibits
git commit -m "Advance submodules to their latest commits"
git push origin main
