
Now create a graph in Mermaid format based on the table of tokens. The mermaid graph type will be `BT`. Whenever we represent a row with a node in the graph, use the "ID" column to identify the node and the "Token" column as the label for the node. 

For all rows that have a non-empty value in the "Link1" column, create a node for that row, then a node for the row with the "ID" value given in the "Link1" column, and use the value of the "Relation1" column as the label for the edge.

For all rows that have a non-empty value in the "Link2" column, create a node for that row, then a node for the row with the "ID" value given in the "Link2" column, and use the value of the "Relation2" column as the label for the edge.
