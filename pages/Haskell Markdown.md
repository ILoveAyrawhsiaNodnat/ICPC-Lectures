- [[All Haskell]]
  [[Haskell Exercises]]
  [[Advent of Code]]
- [ ]  How to write tests?
- [x]  Setup Haskell on vscode with stack.
- [ ]  Haskell repl on vscode.
# Setting up Projects
- We'll going to be using `stack` . Stack's advantage is it generates `.cabal` file automatically from the
- `stack new project` This will create a new directory with the project name and necessary build files.
- `stack setup` will download the compiler if necessary.
- `stack build`
- The new module name should be in capital letters ex - "Parser.hs" not "*parser.hs"*
- `hpack` is the utility which generates `.cabal` file from `package.yaml`.
- `stack build --dry_run` will also do it.
- [https://github.com/commercialhaskell/stack/issues/3697](https://github.com/commercialhaskell/stack/issues/3697) (Adding `stack hpack`)
collapsed:: true
# Types
	- `newtypes` (kind of like alias with one constructor and one param. It creates ismorphic types), `type` (Synonym types), `data`
- NOW [https://wiki.haskell.org/Newtype](https://wiki.haskell.org/Newtype)
  done:: 1623209986120
  later:: 1623210255546
  now:: 1623210255983
  [Advanced Types Haskell](https://en.wikibooks.org/wiki/Yet_Another_Haskell_Tutorial/Type_advanced)
  Consider this:
  
  ```haskell
  data Tree a = Tip | Node a (Tree a) (Tree a)
  Tip :: Tree
  Node :: a -> (Tree a) -> (Tree a) -> (Tree a)
  -- Node is a constructor
  ````Tree` is a type constructor while `Node, Tip` are data constructors.
## [Emacs](https://www.notion.so/Emacs-4d40f0147a7b40de89ee6b0011e891be) setup
- Everything will work immediately on Emacs.
- `C-c C-l` (or `M-x haskell-process-load-file` will load the file in repl)
- Fuck emacs, it's a slow piece of shit.
- Some packages are LTS which will automatically work, but for some non LTS packages, we'll need [https://docs.haskellstack.org/en/stable/GUIDE/#curated-package-sets](https://docs.haskellstack.org/en/stable/GUIDE/#curated-package-sets)
- To add a package, add it in `package.yaml` under `dependencies`.[https://docs.haskellstack.org/en/stable/README/#workflow](https://docs.haskellstack.org/en/stable/README/#workflow)
# Function Currying
	- Function with more than one argument can take a single argument and return another function.
	- This is the first class feature of haskell.