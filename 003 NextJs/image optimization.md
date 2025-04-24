- Using `<Image/>` component
# Why <Image /> comp
- Images are [[optimize bundle size|Lazy loading]] when entering the viewport
-  Serve correctly sized images in modern format(e.g. webb) 
-  Prevents layout shifts
	- by forcing you type width/height properties
	- Warning skipped by
		- ([Statically importing images](https://github.com/ahmad-kashkoush/wild-oasis-website/commit/7941373d9c2ca764bd69e1510393b19300cd5018#r145653545))
		- ([aspect ratio technique commit link](https://github.com/ahmad-kashkoush/wild-oasis-website/commit/7941373d9c2ca764bd69e1510393b19300cd5018#r145665234))
-  Quality can be reduced if needed

