# BigSpicy
## XDM- File Conversion to Xyce format
Primitives and spice files are needed by BigSpicy but they are not processed in their raw format. The files that are fed to BigSpicy should be in Xyce format as minimal internal processing is required for them. 
#### steps to install XDM on debian Linux 
#### Steps to convert file into Xyce format

## Xyce
### 1) Merge SPEF, Verilog and Spice files into circuit protobuf</n>
After obtaining all the required files that is 7nm Primitives and Spice files in Xyce format, netlist and spice files. We need to merge them as in order to generate a spice deck the order of ports for each instantiated module are also required which leads to dependency on PDK. The file we obtain after merging is circuit protobuf file.
#### steps to install Xyce on debian Linux 
#### Steps to merge file to obtain circuit protobuf
##
