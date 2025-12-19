I want to prepare a delimited-text table identifying verbal constructions in a passage of Latin. The table will use the pipe character "|" as the divider, with the following header: "VUID|Token|Depth|Construction|Notes".

The table should include a row for every finite verb form, every participle, and every infinitive used in indirect statement. It should omit infinitives used as nouns (e.g., in "Legere bonum est", omit "Legere" since it is simply the subject of the verb "est"). Treat complementary infinitives as part of a single verbal expression (e.g., in "intellegere non possum"), treat the two words "intellegere possum" as the verbal expression).

In each row, assign a unique numeric identifier to the "VUID" column, and list the form of the verb in the "Token" column.

For finite verbs, if it is a primary (main) verb, add "primary verb" to the "Construction" column; if it is a secondary (subordinate) verb, add "secondary verb"; if it is a participle, add "participle"; if it is an infinitive in indirect statement, add "indirect statement".

The "Depth" column should be an integer value listing the syntactic depth of the verbal expression, starting from depth 1 for primary verbs. Example: "donum ei, qui postquam Trioa capta erat, ad nos venit, dedi." Has three verbal expressions. "dedi" is the primary verb, so depth 1. "venit" is the verb of a relative clause directly dependent on the primary clause, so depth 2. "capta erat" is the verb of a secondary clause dependent on the secondary clause "qui ad nos venit", so depth 3.
