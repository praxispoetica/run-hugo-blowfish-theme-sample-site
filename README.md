# Setup and run Hugo Blowfish theme `exampleSite` locally

- [Blowfish Site](https://blowfish.page/)
- [Github repo](https://github.com/victorkane/run-hugo-blowfish-theme-sample-site/blob/main/README.md)

## Create a new Hugo site

```bash
victor@victorpc:dev$ hugo new site exampleSite
Congratulations! Your new Hugo site was created in /home/victor/Work/Learn/Hugo/Blowfish/dev/exampleSite.

Just a few more steps...

1. Change the current directory to /home/victor/Work/Learn/Hugo/Blowfish/dev/exampleSite.
2. Create or install a theme:
   - Create a new theme with the command "hugo new theme <THEMENAME>"
   - Install a theme from https://themes.gohugo.io/
3. Edit hugo.toml, setting the "theme" property to the theme name.
4. Create new content with the command "hugo new content <SECTIONNAME>/<FILENAME>.<FORMAT>".
5. Start the embedded web server with the command "hugo server --buildDrafts".

See documentation at https://gohugo.io/.
victor@victorpc:dev$ cd
exampleSite/ mywebsite/
victor@victorpc:dev$ cd exampleSite/
victor@victorpc:exampleSite$ pwd
/home/victor/Work/Learn/Hugo/Blowfish/dev/exampleSite
```

## Download the Blowfish theme in VS Code terminal as git submodule

```bash
victor@victorpc:exampleSite$ git init
Initialized empty Git repository in /home/victor/Work/Learn/Hugo/Blowfish/dev/exampleSite/.git/
victor@victorpc:exampleSite$ git submodule add -b main https://github.com/nunocoracao/blowfish.git themes/blowfish
Cloning into '/home/victor/Work/Learn/Hugo/Blowfish/dev/exampleSite/themes/blowfish'...
remote: Enumerating objects: 24421, done.
remote: Counting objects: 100% (94/94), done.
remote: Compressing objects: 100% (67/67), done.
remote: Total 24421 (delta 46), reused 60 (delta 26), pack-reused 24327
Receiving objects: 100% (24421/24421), 383.98 MiB | 34.40 MiB/s, done.
Resolving deltas: 100% (11517/11517), done.
victor@victorpc:exampleSite$ code .
```

## Copy `themes/blowfish/exampleSite` folders and files into project root

- Recursive copy should be sufficient

## Run locally

```bash
victor@victorpc:exampleSite$ hugo server
Watching for changes in /home/victor/Work/Learn/Hugo/Blowfish/dev/exampleSite/{archetypes,assets,content,data,i18n,layouts,static,themes}
Watching for config changes in /home/victor/Work/Learn/Hugo/Blowfish/dev/exampleSite/hugo.toml, /home/victor/Work/Learn/Hugo/Blowfish/dev/exampleSite/config/_default, /home/victor/Work/Learn/Hugo/Blowfish/dev/exampleSite/themes/blowfish/config.toml, /home/victor/Work/Learn/Hugo/Blowfish/dev/exampleSite/themes/blowfish/config/_default
Start building sites …
hugo v0.120.4-f11bca5fec2ebb3a02727fb2a5cfb08da96fd9df+extended linux/amd64 BuildDate=2023-11-08T11:18:07Z VendorInfo=gohugoio


                   | EN
-------------------+------
  Pages            | 187
  Paginator pages  |   0
  Non-page files   |  87
  Static files     |   8
  Processed images | 152
  Aliases          |  74
  Sitemaps         |   1
  Cleaned          |   0

Built in 6354 ms
Environment: "development"
Serving pages from memory
Running in Fast Render Mode. For full rebuilds on change: hugo server --disableFastRender
Web Server is available at http://localhost:1313/blowfish/ (bind address 127.0.0.1)
Press Ctrl+C to stop
```
