# Qt5 for Broadsoft UC One

This repository contains acute patches for the Qt5 needed by UC One.

We will use Qt projects `init-repository` for setting up the submodules. This script should be always run in the branch `ucone/dev`.
The script expects that the remote *origin* points to official Qt repositories.

If you just cloned this repository, please fix this by:

    cd qt5

    git remote rename origin mirror
    git remote add origin git://code.qt.io/qt/qt5.git

Then run the `init-repository` script using switch *mirror* e.g:

    perl init-repository --mirror "git@github.com/Broadsoft/"

This will setup the submodule URLs and clone all the submodules.
The remote *mirror* is used as the primary source for clones. If some
of the submodules do not exist on the mirror (Broadsoft Qt fork),
the init script will automatically fall-back to the official
Qt repositories (based on remote *origin*).

Once you have successfully cloned the submodules, you can proceed to
checkout the version branch e.g. `ucone/5.5.1`.

Otherwise please refer to the Qt project [README](README)
