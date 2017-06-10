# URL to Markdown
A very very simple command line function making use of [Fuck Yeah Markdown](http://fuckyeahmarkdown.com)’s API to convert a given URL to a markdown formatted file.

## Usage
`curl --data "u=[URL]" http://fuckyeahmarkdown.com/go/ > ~/Desktop/post.md`

## Shortcut
In order to provide some convenience by being able to more easily access this functionality, one can define a command line function like so:

```
md() {
  curl --data "u=$1" http://fuckyeahmarkdown.com/go/ > ~/Desktop/post.md
}
```

Put the above code into your `.*rc` file whether it be `.bashrc`, `.zshrc` or any other flavour of yours.

Don’t forget to start a new command line session as the function won’t be recognised by your current session!

And voila! Now all you have to is:

`md [URL]`

## Limitations
Even though [Fuck Yeah Markdown](http://fuckyeahmarkdown.com) provides some great functionality, unfortunately, it’s not bullet proof. Occasionally, it might be unable to parse the given URL and other times even though it parses, the output might contain some junk.
