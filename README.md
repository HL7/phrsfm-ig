PHR-S Functional Model R2 to FHIR Requirements-based representation and publication with the Common HL7 Toolset (FHIR IG)

## Running the scipt and IG publisher

### Convert script
```
> docker run --name=phrsfm-ig -it -v "$(pwd)":/app node:latest /bin/bash
@> (once) dpkg -i jdk-23_linux-x64_bin.deb
@> (once) apt -y update; apt -y install graphviz jekyll
@> (once) git config --global --add safe.directory /app
@> cd script
@> (once) npm install
@> node max2fhir.js
@> node max2plantuml.js > ../input/images-source/relationships.plantuml 
```

Update groupings and resources from output.txt in phrs-ig.json

### To build IG
```
(optional)> curl -L https://github.com/HL7/fhir-ig-publisher/releases/latest/download/publisher.jar -o input-cache/publisher.jar
@> java -jar input-cache/publisher.jar -ig ig.ini
```
