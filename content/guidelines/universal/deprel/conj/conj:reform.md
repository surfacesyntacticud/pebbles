---
title: conj:reform
request: pattern { X -[1=conj, 2=reform]-> Y }
scope:
  schema: SUD
type: doc
tags:
 - spoken
 - deprel
---


The `conj:reform` relation is specific to spoken language and it is used to link elements in a reformulation.
The first element id a complete utterance (for uncomplete utterence, the [`repair`](guidelines/universal/deprel/repair) relation is used).
The second element is similar (often reusin gthe same wording and giving more details) and can replaced the first one. 

<conll>
# lang = French
# text = en fait j'habite dans une maison en banlieue, la banlieue parisienne.
# sent_id = ParisStories_2019_histoireDeBanlieue_2
# speaker = non_native
1	en	en	ADP	_	ExtPos=ADV	4	discourse	_	Idiom=Yes
2	fait	fait	NOUN	_	_	1	comp	_	Gender[lex]=Masc|InIdiom=Yes|Number[ctxt]=Sing
3	j'	moi	PRON	_	Case=Nom|Emph=No|PronType=Prs	4	subj	_	Number[lex]=Sing|Person[lex]=1|SpaceAfter=No
4	habite	habiter	VERB	_	Mood=Ind|Number=Sing|Tense=Pres|VerbForm=Fin	0	root	_	Person[ctxt]=1
5	dans	dans	ADP	_	_	4	comp:obl	_	_
6	une	un	DET	_	Definite=Ind|Gender=Fem|Number=Sing|PronType=Art	7	det	_	_
7	maison	maison	NOUN	_	_	5	comp	_	Gender[lex]=Fem|Number[ctxt]=Sing
8	en	en	ADP	_	_	4	discourse	_	_
9	banlieue	banlieue	NOUN	_	_	8	comp	_	Gender[lex]=Fem|Number[ctxt]=Sing|SpaceAfter=No|highlight=red
10	,	,	PUNCT	_	_	12	punct	_	_
11	la	le	DET	_	Definite=Def|Gender=Fem|Number=Sing|PronType=Art	12	det	_	HasSpokenGender=OnlySingExceptWithLiaison
12	banlieue	banlieue	NOUN	_	_	9	conj:reform	_	Gender[lex]=Fem|Number[ctxt]=Sing|highlight=red
13	parisienne	parisien	ADJ	_	Gender=Fem	12	mod	_	HasSpokenGender=YesExceptSingWithLiaison|HasSpokenNumber=OnlyWithLiaison|Number[ctxt]=Sing|SpaceAfter=No
14	.	.	PUNCT	_	_	4	punct	_	_
</conll>


Whereas the relation [`conj:coord`](./conj:coord.md) links two different objects, two referents (ex: *Mary and John* are two different referents).
The relation `conj:reform`, on the other hand, is used to link two denotations of the same referent (ex: *the desert in Kenya, the Kenya desert* is denoting the same referent).

<conll>
# lang = French
# text = puisque les les les les c~ les capitales les grandes villes ne me disaient rien du tout
# text_en = since I didn't know anything at all about the the the the c ~ the capitals the big cities
1	puisque	puisque	SCONJ	_	_	0	root	_	Gloss=since
2	les	le	DET	_	Definite=Def|Number=Plur|PronType=Art	6	det	_	Gloss=the
3	les	le	DET	_	Definite=Def|Number=Plur|PronType=Art	2	repair	_	Gloss=the
4	les	le	DET	_	Definite=Def|Number=Plur|PronType=Art	3	repair	_	Gloss=the
5	les	le	DET	_	Definite=Def|Number=Plur|PronType=Art	4	repair	_	Gloss=the
6	c~	c~	X	_	_	14	subj	_	_
7	les	le	DET	_	Definite=Def|Number=Plur|PronType=Art	8	det	_	Gloss=the
8	capitales	capitale	NOUN	_	Gender=Fem|Number=Plur	6	repair	_	Gloss=capitals|highlight=red
9	les	le	DET	_	Definite=Def|Number=Plur|PronType=Art	11	det	_	Gloss=the
10	grandes	grand	ADJ	_	Gender=Fem|Number=Plur	11	mod	_	Gloss=big
11	villes	ville	NOUN	_	Gender=Fem|Number=Plur	8	conj:reform	_	Gloss=cities|highlight=red
12	ne	ne	ADV	_	Polarity=Neg	14	mod	_	Gloss=not
13	me	lui	PRON	_	_	14	comp:obl	_	Gloss=me
14	disaient	dire	VERB	_	Mood=Ind|Number=Plur|Person=3|Tense=Imp|VerbForm=Fin	1	comp	_	Gloss=tell
15	rien	rien	PRON	_	_	14	comp:obj	_	Gloss=nothing
16	du	du	ADP	_	_	15	mod	_	Gloss=of_the
17	tout	tout	ADV	_	_	16	comp	_	Gloss=all
</conll>




