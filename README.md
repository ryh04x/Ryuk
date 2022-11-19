## Description:
<!-- ALL-CONTRIBUTORS-BADGE:START - Do not remove or modify this section -->
[![All Contributors](https://img.shields.io/badge/all_contributors-1-orange.svg?style=flat-square)](#contributors-)
<!-- ALL-CONTRIBUTORS-BADGE:END -->

Bash script for Subdomain Enumeration using 4 tools and 3 online services, you have to install these tools by yourself to be able to use ryuk.sh, or use [setup.sh](https://github.com/ryh04x/Ryuk/blob/master/setup.sh) script to install them.

![image](img.png)

### Available Tools and online services:

1. Tools:
	- [Findomain](https://github.com/Edu4rdSHL/findomain)
	- [SubFinder](https://github.com/projectdiscovery/subfinder)
	- [Amass](https://github.com/OWASP/Amass)
	- [AssetFinder](https://github.com/tomnomnom/assetfinder)
	- [Httprobe](https://github.com/tomnomnom/httprobe): To Probe For Working HTTP and HTTPS Subdomains.
	- [anew](https://github.com/tomnomnom/anew): To delete duplicates when using -s/--silent option.
1. online services:
	- [WayBackMachine](http://web.archive.org/)
	- [crt.sh](https://crt.sh/)
	- [BufferOver](https://dns.bufferover.run/)

## Installation:

to install the dependencies run:

```bash
$ git clone https://github.com/ryh04x/Ryuk.git
$ cd Ryuk
$ chmod +x setup.sh
$ ./setup.sh
```

## Usage:

### Basic usage:

```bash
$ ryuk -d target.com 
```

### Resolve The Found Subdomains:

```bash
$ ryuk -d target.com -r 
```

### Agains a list of domains

```bash
$ ryuk -l domains.txt -r
```

### Exclude:

```bash
$ ryuk -d target.com -e Amass,wayback
```

### Use:

```bash
$ ryuk -d target.com -u Findomain,Subfinder
```

exclude and use can be used with list of domains too 

```bash
$ ryuk -l domains.txt -u crt,bufferover
```

### Parallel:
the tool `parallel` must be installed on you system, it runs all the functions at the same time which make the results faster, doesn't work with -u/--use or -e/--exclude options.

```bash
$ ryuk -d target.com -p
```


### Silent:

this option helps when you want to pipe the results to another tool, or just to avoid the useless output.

```bash
$ ryuk -d target.com -s 
dev.target.com
admin.target.com
api.target.com
..
..
```

happy hacking!

## Contributors ✨

Thanks goes to these wonderful people ([emoji key](https://allcontributors.org/docs/en/emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->
<table>
  <tr>
    <td align="center"><a href="https://github.com/secfb"><img src="https://avatars.githubusercontent.com/u/105162677?s=400&u=cb9a46dd4d17076dc18e90139743aa427814f888&v=40" width="100px;" alt=""/><br /><sub><b>Kashish Kanojia</b></sub></a><br /><a href="https://github.com/ryh04x/Ryuk/commits?author=secfb" title="Code">💻</a></td>
  </tr>
</table>

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/all-contributors/all-contributors) specification. Contributions of any kind welcome!
