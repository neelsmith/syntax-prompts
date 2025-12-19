### USER
I want to prepare a delimited-text table using the pipe character "|" as the divider summarizing syntactic features of this passage of Latin. The table should have 7 columns labelled:
ID|Token|Link1|Relation1|Link2|Relation2|Notes
Begin by populating the `ID` and `Token` columns as follows. Separate the text into word tokens, treating enclitics as separate word tokens, but treating compound verb forms such as the perfect passive as a single token; ignore punctuation, and number the resulting list sequentially. E.g. given the phrase "arma virumque cano, Troiae" you would add 5 rows numbered 1-5 for the tokens "arma", "virum", "que",  "cano" and "Troiae" (ignoring "," and separating "virumque" into 2 tokens); given "Caesar interfectus est" you add 2 rows for the tokens "Caesar" and "interfectus est".
Next, for every finite (conjugated) verb form, add the following to the "Notes" column: if it is a primary (main) verb, add "primary", if it is a secondary (subordinate) verb, add "secondary". If a primary verb is introduced by a coordinating conjunction, add the ID and Token for that conjunction to the "Link1" column of the primary verb, and add the word "main verb" to the "Relation1" column of the primary verb. For each secondary verb, add the ID and token of the subordinating word (relative pronoun, subordinate conjunction, etc.) to the "Link1" column of the secondary verb, and add the word "subordinate verb" to "Relation2" of the secondary verb.

### ASSISTANT
ID|Token|Link1|Relation1|Link2|Relation2|Notes
1|ac|||||
2|plerique|||||
3|suam|||||
4|ipsi|||||
5|vitam|||||
6|narrare|||||
7|fiduciam|||||
8|potius|||||
9|morum|||||
10|quam|||||
11|adrogantiam|||||
12|arbitrati sunt|1 ac|main verb|||primary
13|nec|||||
14|id|||||
15|Rutilio|||||
16|et|||||
17|Scauro|||||
18|citra|||||
19|fidem|||||
20|aut|||||
21|obtrectationi|||||
22|fuit|13 nec|main verb|||primary
23|adeo|||||
24|virtutes|||||
25|isdem|||||
26|temporibus|||||
27|optime|||||
28|aestimantur|||||primary
29|quibus|||||
30|facillime|||||
31|gignuntur|29 quibus|||subordinate verb|secondary
32|at|||||
33|nunc|||||
34|narraturo|||||
35|mihi|||||
36|vitam|||||
37|defuncti|||||
38|hominis|||||
39|venia|||||
40|opus|||||
41|fuit|32 at|main verb|||primary
42|quam|||||
43|non|||||
44|petissem|42 quam|||subordinate verb|secondary
45|incusaturus|||||
46|tam|||||
47|saeva|||||
48|et|||||
49|infesta|||||
50|virtutibus|||||
51|tempora|||||

### USER
Next for every noun or pronoun functioning as the subject of a verb, add the ID and token for the verb to the "Link1" column of the noun, and "subject" to the "Relation1" column of the noun. For every noun or pronoun functioning as the object of a verb, add the ID and token for the verb to the "Link1" column of the noun, and "subject" to the "Relation1" column of the noun.

### ASSISTANT
ID|Token|Link1|Relation1|Link2|Relation2|Notes
1|ac|||||
2|plerique|12 arbitrati sunt|subject|||
3|suam|||||
4|ipsi|12 arbitrati sunt|subject|||
5|vitam|6 narrare|subject|||
6|narrare|||||
7|fiduciam|||||
8|potius|||||
9|morum|||||
10|quam|||||
11|adrogantiam|||||
12|arbitrati sunt|1 ac|main verb|||primary
13|nec|||||
14|id|22 fuit|subject|||
15|Rutilio|||||
16|et|||||
17|Scauro|||||
18|citra|||||
19|fidem|||||
20|aut|||||
21|obtrectationi|||||
22|fuit|13 nec|main verb|||primary
23|adeo|||||
24|virtutes|28 aestimantur|subject|||
25|isdem|||||
26|temporibus|||||
27|optime|||||
28|aestimantur|||||primary
29|quibus|||||
30|facillime|||||
31|gignuntur|29 quibus|||subordinate verb|secondary
32|at|||||
33|nunc|||||
34|narraturo|||||
35|mihi|||||
36|vitam|34 narraturo|subject|||
37|defuncti|||||
38|hominis|||||
39|venia|41 fuit|subject|||
40|opus|||||
41|fuit|32 at|main verb|||primary
42|quam|44 petissem|subject|||
43|non|||||
44|petissem|42 quam|||subordinate verb|secondary
45|incusaturus|||||
46|tam|||||
47|saeva|||||
48|et|||||
49|infesta|||||
50|virtutibus|||||
51|tempora|||||