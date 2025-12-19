
I want to create a graph in Mermaid format based on a table with 7 columns delimited by the pipe character, labelled `ID|Token|Link1|Relation1|Link2|Relation2|Notes`. The mermaid graph type will be `BT`. Whenever we represent a row with a node in the graph, use the "Token" column as the label for the node.

First create nodes for each row with the value "main verb" in the "Relation1" column. Label the node with the value of the "Token" column. If the row has a non-empty value for "Link1", the integer beginning that value is the ID for a row to link. E.g. if the value of "Link1" was "32 at", then we want to create an edge from the "main verb" node to the node with ID "32". The edge should be labelled "verb". 




Next for each main verb, check for any rows with a "Link1" vaue beginning with the integer ID of the main verb. Create a link from a node for that row to the main verb. The edge should be labelled with the value of that row's "Relation1" column. 