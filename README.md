# BigSpicy
## XDM- File Conversion to Xyce format
Primitives and spice files are needed by BigSpicy but they are not processed in their raw format. The files that are fed to BigSpicy should be in Xyce format as minimal internal processing is required for them. 
#### steps to install XDM on debian Linux 
#### Steps to convert file into Xyce format

## Xyce
### 1) Merge SPEF, Verilog and Spice files into circuit protobuf</n>
After obtaining all the required files that is, 7nm Primitives and Spice files in Xyce format, netlist and spice files. We need to merge them as in order to generate a spice deck the order of ports for each instantiated module are also required which leads to dependency on PDK. We then convert the merged files into protobuf with the help of protoc. 

#### steps to install Xyce on debian Linux 
#### Steps to install protoc
#### Steps to merge file to obtain circuit protobuf
## 2) Generating Module Spice Model and Transistor level Spice
The protobuf file that we have generated in the previous step and PDK spice file are then used to make a whole module spice model.<\n>
We then pass the ```--flatten_spice``` argument to convert the whole module spice model into transistor level spice.
## 3) Generating test to measure input capacitance
We take the protobuf file, PDK primitives file and the spice file of our module to generate the test manifest and circuit analysis protobuf files. We then run Xyce to perform tests. 
## 4) Linear and transient analysis
we then perform the linear and transient analysis using Xyce with the help of test manifest and circuit analysis protobuf files. 
## 5) Generating wire and whole module tests
We take the protobuf file, primitives, spice, test manifest and circuit analysis file to generate test for whole module. 
  
## perform analysis on wire and whole module tests
We take Final.pb, PDK primitives, test_manifest, test_analysis, PDK spice decks. Input capacitance and delays will be analysed.
