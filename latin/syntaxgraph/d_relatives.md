For each relative pronoun, if it has an explicit antecedent, add the ID and Token for the antecedent to the "Link2" column of the adjective, and add the word "antecedent" to the "Relation2" column of the adjective.

If it does not have an explicit antecedent, then find the function of the implied antecedent in the superior clause as follows:


1. if the implied antecedent subject of a verb form, add the ID and Token for the verb to "Link1" column of the relative pronoun, and add the word "subject" to "Relation1" column.
2. if direct object of a verb form, add the ID and Token for the verb to "Link1" column, and add the string "object " + the case of the object to "Relation1" column.
3. if a predicate noun or pronoun, add the ID and Token for the verb to "Link1" column, and add the string "predicate noun" + the case of the object to "Relation1" column. Make the "VUID" the same as the "VUID" of the verb.
4. if the object of a preposition, add the ID and Token for the preposition to "Link1" column and the string "object of preposition" to "Relation1" column.
5. if related to the verb by usage in the dative case (such as indirect object) or ablative case (such as ablative of means or instrument), add the ID and Token for the verb to "Link1" column and the case of the substantive to "Relation1" column. Make the "VUID" the same as the "VUID" of the verb.
6. if related to another substantive by usage in the genitive case (such as possessive, e.g., "eius liber"), add the ID and Token for the substantive to "Link1" column and word "genitive" to "Relation1" column. Make the "VUID" the same as the "VUID" of the other substantive.