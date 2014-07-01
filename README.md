Ewe2's insane project to GPL GZDoom.
====================================

Rationale: make a gzdoom port that builds well on linux at least and avoids
some of the more stupid excesses of zdoom, and supports GPL. Don't hold your
breath, I'm not a top coder.

From the discussion on
http://www.doomworld.com/vb/source-ports/58608-make-a-gpl-fork-of-gzdoom the
following issues arise:

* Build code is problematic: software renderer is an issue in this regard, but
  dependencies are littered through several files.
* oplsynth code is a problem. Ironically, they've partially implemented the
  same dosbox opl code as chocolate doom.
* openAL is a problem, but we want to avoid it anyway.
* output_sdl will need a rewrite obviously.


Check docs/fmod-dep and docs/silverman-dep for problem files.
Reference kenbuild.zip and jfbuild_src20050531.zip for the actual Build
sourcecode. We probably need to carefully compare where this stuff is, its
mostly math routines and rendering.

Cons:
* means removing a lot of sound effects that people apparently like.
* means possibly rewriting major rendering code, which i am definitely not
  qualified to do.
* will definitely affect cross-platform compatibility, but I'm not qualified
  to track windows/osx compatibility anyway, that can be someone else's
  problem.

Pros:
* Tracking FMOD code is a fool's errand anyway, it's too big and too
  controlling.

