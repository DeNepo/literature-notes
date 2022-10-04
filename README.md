# Literature notes

This will eventually be a visual graph displaying the relationships between the relevant articles, papers, and blog posts. For now, we're just trying to get it running locally.

## Running locally

1. Download [hugo-obsidian](https://github.com/jackyzha0/hugo-obsidian) and build the executable locally. For linux/MacOS, that means cloning the repository, running `go build -o hugo-obsidian ./`, making the output file executable with `chmod +x hugo-obsidian`, and then placing it in your path (maybe at `/usr/bin/hugo-obsidian`. You can test it's set up by running `hugo obsidian`, and you should see output like the following:

```
Scraping .
[DONE] in 2ms
Ignored 0 private files 
Parsed 0 total links 
Removed 0 external and non-markdown links
```

2. Download [hugo](https://github.com/gohugoio/hugo/releases), and make sure you get one of the `hugo_extended` releases. For linux/MacOS, unzip it and move the binary to your path, like at `/usr/local/bin/hugo`. Test your installation by running `hugo version`. The output should be something like:

```
hugo v0.104.1-8958b8741f552c8024af5194330fbf031544a826+extended linux/amd64 BuildDate=2022-09-26T17:05:45Z VendorInfo=gohugoio
```

3. Now, you're ready to serve it locally via the Makefile command `make serve`. You should have a running server locally at `http://localhost:1313`.

4. Profit
