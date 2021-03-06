# dot-graphviz
This project is another Proof of Value by Raul Andres to develop an idea to generate Architecture diagrams using dot language + graphviz + aws icons + git . Lets start to create and modify Architecture diagrams in agile way! ;) Architecture as a code AaaC will become soon ;)

This idea Raul Andres thought 2 years ago to agilize the Architecture Governance workflow and now it is the time to create the solution and put in practice.

The goals is to personally reuse this technic to be more efficient and agile in the next Architecture jobs he will do.

It uses AWS icons but it could be used with any icons library creating another xxx-icons folder.

Please feel free to reuse and hack it, enjoy!

## MT Challenge example
Raul Andres was challenged by MT company(masking the company name, but it is a real company) to do a Case-Study for an interview process and he decided to create the diagrams with code and later reuse his effort to build the next diagrams.

## Architecture Diagrams generated

* Data Pipeline Architecture Reference (WIP)
* AWS E2E Architecture References

The rest of architecture artefacts generated is in the folder [diagrams](https://github.com/manilabay/dot-graphviz-aws/diagrams/)

### MT-logical-architecture  

![MT-logical-architecture](diagrams/mt-challenge-solution/mt-logical-architecture.png?raw=true "MT-logical-architecture")

### MT-technical-architecture  

![MT-technical-architecture](diagrams/mt-challenge-solution/mt-technical-architecture.png?raw=true "MT-technical-architecture")

Basically and to understand very clear the diagram:

* Green arrows represent end-to-end solution User traffic
* Blue arrows represent internal processing traffic
* Red arrows represent update/release traffic

## How to use

0. Learn dot language and graphviz. To see some References below.
1. Create a new folder inside diagrams folder
2. Create new README.md inside that new folder, using [this] https://github/manilabay/dot-graphviz-aws/diagrams/mt-challenge-solution/README.md as a template.
3. Create dot code for the diagram you want create using language-dot syntax
4. Convert dot file to png (see below)
5. Show and share the diagrams and knowledge with your Architect mates.
6. Get some reward, a coffee, a beer or why not a salary increase ;)

## How to convert dot code to graph

### Using Docker convert container
You could use [my another repo](https://github.com/manilabay/docker-graphviz-png-cli) to build a docker container convert tool, so you dont need to install dependencies and reuse it.

Once you have the tool image built you could run:
```console
cat input.dot | docker run -v your-host-path-or-Volume:/aws-icons --rm -i graphv
iz-convert-png > output.png
```

### Using dot command

```console
dot -Tpng input.dot > output.png
```

As a example to create the diagram for the mt-logical-architecture you must run:

```console
dot -Tpng mt-logical-architecture.dot > mt-logical-architecture.png
```

## Dependencies

* [Graphviz](https://aws.amazon.com/architecture/icons/)
* [Dot languages](https://aws.amazon.com/architecture/icons/)

### AWS icons
This is the Official AWS icons collection downloaded from
* [AWS Simple Icons for Architecture Diagrams](https://aws.amazon.com/architecture/icons/)

**This icons material and folder belongs to Amazon Web Services, Inc. or its affiliates and all trademarks belongs to Amazon Web Services, Inc. or its affiliates.**

**Please don't download from this GIT Repo due the AWS upgrades.**

## References

[Learn Dot language](https://www.graphviz.org/doc/info/lang.html)
[Learn Graphviz language](https://www.graphviz.org)

## TODO

* Create a docker image with dot and graphviz to use as a function to generate graphviz object onfly. Atm you could use this [simple command](https://github.com/manilabay/dot-graphviz-aws/tree/master/diagrams)
