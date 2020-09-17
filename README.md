# figwheel-example

## Overview

Demonstrate an issue with figwheel and a possible solution.

## Reproduce

1. Delete [this](https://github.com/komcrad/figwheel-example/blob/master/src/hello_world/core.cljs#L20) line in your local branch and save file.
2. Run `lein fig:build`
3. Revert step 1. Add `[[]]` back. Save file.
4. Figwheel will load a blank page.
5. Repeat step one. Save file.
6. Figwheel will still load a blank page.
7. Execute `:cljs/quit` in figwheel repl

## Possible Solution

[This](https://github.com/komcrad/figwheel-core/commit/05fe7c0d2455f4b21df216664796998524200b4a) commit should fix the issue.
1. Clone https://github.com/komcrad/figwheel-core
2. Configure project.clj to be version 2.11.0
3. `lein install`
4. Repeat steps in the 'Reproduce' section. Step 6 should be false.
