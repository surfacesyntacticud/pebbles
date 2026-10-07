---
title: reparandum
request: pattern { X -[reparandum]-> Y }
scope:
  schema: SUD
type: doc
tags:
 - deprel
 - spoken
---

This relation is used to indicate difluencies, such as when a speaker corrects their speech.
It is similar to the [`reparandum` UD relation](https://universaldependencies.org/u/dep/reparandum.html), but in SUD, especially for spoken data, it is in in concurrence with [`conj:reform`](https://pebbles.surfacesyntacticud.org/guidelines/universal/deprel/conj/conj:reform). 

`reparandum`is a relation between a reparandum and its repair. Two cases are possible :

1) the reparandum that do not contain a complete content word (it can contain an unfinished content word): 

<conll>
# lang = French
# sent_id = ParisStories_2019_stagePrimaire_15
# text = j'ai j'ai vraiment adoré ce côté là .
# text_en = I did I did really like that part
1	j'	moi	PRON	_	Number[lex]=Sing|Person[lex]=1|PronType=Prs	2	subj	_	SpaceAfter=No|Gloss=I
2	ai	avoir	AUX	_	Number=Sing|Person=1	4	reparandum	_	Gloss=have|highlight=red
3	j'	moi	PRON	_	Number[lex]=Sing|Person[lex]=1|PronType=Prs	4	subj	_	SpaceAfter=No|Gloss=I
4	ai	avoir	AUX	_	Mood=Ind|Number=Sing|Person=1|Tense=Pres|VerbForm=Fin	0	root	_	Gloss=have|highlight=red
5	vraiment	vraiment	ADV	_	_	6	mod	_	Gloss=really
6	adoré	adorer	VERB	_	Gender=Masc|Number=Sing|Tense=Past|VerbForm=Part	4	comp:aux	_	Gloss=loved
7	ce	ce	DET	_	_	8	det	_	Gloss=that
8	côté	côté	NOUN	_	Gender=Masc|Number=Sing	6	comp:obj	_	Gloss=part
9	là	là	ADV	_	_	8	mod	_	Gloss=that
10	.	.	PUNCT	_	_	_	_	_	_
</conll>

2) the reparandum contains content words, but it is an incomplete unit and all the content words are repeated in the repair.

<conll>
# sent_id = Rhap_D2008-126
# text = donc, euh, le scénario auquel on peut s'attendre encore une fois avec toutes les précautions qu'il faut, d'usage, qu'il faut mettre, c'est que cette souche que l'on voit en Amérique du Nord ne va pas se plaire beaucoup avec l'été, euh, chez nous, dans l'hémisphère nord.
# text_en = So, um, the scenario we can expect once again taking all the precautions that need, required, that need to be taken, it's that this strain we're seeing in North America won't fare very well during the summer, um, here in the Northern Hemisphere.
1	donc	donc	ADV	_	_	32	mod	_	SpaceAfter=No|WordAlignmentBegin=358892|WordAlignmentEnd=359227
2	,	,	PUNCT	_	_	1	punct	_	WordAlignmentBegin=359227|WordAlignmentEnd=359227
3	euh	euh	INTJ	_	_	32	discourse:filler	_	SpaceAfter=No|WordAlignmentBegin=359227|WordAlignmentEnd=359446
4	,	,	PUNCT	_	_	3	punct	_	WordAlignmentBegin=359446|WordAlignmentEnd=359551
5	le	le	DET	_	Definite=Def|Gender=Masc|Number=Sing|PronType=Art	6	det	_	HasSpokenGender=OnlySingExceptWithLiaison|WordAlignmentBegin=359551|WordAlignmentEnd=359676
6	scénario	scénario	NOUN	_	_	32	dislocated:subj	_	Gender[lex]=Masc|Number[ctxt]=Sing|WordAlignmentBegin=359676|WordAlignmentEnd=360381
7	auquel	lequel	PRON	_	Gender=Masc|Number=Sing|PronType=Rel	11	comp:obl	_	WordAlignmentBegin=361187|WordAlignmentEnd=361392
8	on	on	PRON	_	Case=Nom|Emph=No|PronType=Ind	9	subj	_	Gender[ctxt]=Masc|Number[lex]=Sing|Person[lex]=3|WordAlignmentBegin=361392|WordAlignmentEnd=361472
9	peut	pouvoir	VERB	_	Mood=Ind|Number=Sing|Tense=Pres|VerbForm=Fin	6	mod@relcl	_	Person[ctxt]=3|WordAlignmentBegin=361472|WordAlignmentEnd=361662
10	s'	soi	PRON	_	PronType=Prs|Reflex=Yes	11	comp@expl	_	Person[lex]=3|SpaceAfter=No|WordAlignmentBegin=361662|WordAlignmentEnd=361732
11	attendre	attendre	VERB	_	VerbForm=Inf	9	comp:obj	_	Subject=SubjRaising|WordAlignmentBegin=361732|WordAlignmentEnd=362212
12	encore	encore	ADV	_	_	9	mod	_	WordAlignmentBegin=362212|WordAlignmentEnd=362462
13	une	un	DET	_	Definite=Ind|Gender=Fem|Number=Sing|PronType=Art	14	det	_	WordAlignmentBegin=362462|WordAlignmentEnd=362522
14	fois	fois	NOUN	_	_	12	mod	_	Gender[lex]=Fem|Number[ctxt]=Sing|WordAlignmentBegin=362522|WordAlignmentEnd=362962
15	avec	avec	ADP	_	_	9	mod	_	WordAlignmentBegin=363079|WordAlignmentEnd=363444
16	toutes	tout	ADJ	_	Gender=Fem	18	mod	_	HasSpokenGender=YesExceptSingWithLiaison|HasSpokenNumber=OnlyWithLiaison|Number[ctxt]=Plur|WordAlignmentBegin=363444|WordAlignmentEnd=363704
17	les	le	DET	_	Definite=Def|Number=Plur|PronType=Art	18	det	_	HasSpokenGender=OnlySingExceptWithLiaison|WordAlignmentBegin=363704|WordAlignmentEnd=363774
18	précautions	précaution	NOUN	_	_	15	comp	_	Gender[lex]=Fem|Number[ctxt]=Plur|WordAlignmentBegin=363774|WordAlignmentEnd=364314
19	qu'	que	PRON	_	PronType=Rel	21	comp:obj	_	SpaceAfter=No|WordAlignmentBegin=364314|WordAlignmentEnd=364384|highlight=red
20	il	lui	PRON	_	Case=Nom|Emph=No|Gender=Masc|Number=Sing|PronType=Prs|Shared=No	21	subj@expl	_	Person[lex]=3|WordAlignmentBegin=364384|WordAlignmentEnd=364454|highlight=red
21	faut	falloir	VERB	_	Mood=Ind|Number=Sing|Tense=Pres|VerbForm=Fin	28	reparandum	_	Person[ctxt]=3|SpaceAfter=No|WordAlignmentBegin=364454|WordAlignmentEnd=364944|highlight=red
22	,	,	PUNCT	_	_	21	punct	_	WordAlignmentBegin=364944|WordAlignmentEnd=364944
23	d'	de	ADP	_	_	18	udep	_	SpaceAfter=No|WordAlignmentBegin=364944|WordAlignmentEnd=365034
24	usage	usage	NOUN	_	_	23	comp	_	Gender[lex]=Masc|LiaisonPossibleBefore=Yes|Number[ctxt]=Sing|SpaceAfter=No|WordAlignmentBegin=365034|WordAlignmentEnd=365344
25	,	,	PUNCT	_	_	23	punct	_	WordAlignmentBegin=365344|WordAlignmentEnd=365344
26	qu'	que	PRON	_	PronType=Rel	29	comp:obj	_	SpaceAfter=No|WordAlignmentBegin=365344|WordAlignmentEnd=365394
27	il	lui	PRON	_	Case=Nom|Emph=No|Gender=Masc|Number=Sing|PronType=Prs	28	subj@expl	_	Person[lex]=3|WordAlignmentBegin=365394|WordAlignmentEnd=365464
28	faut	falloir	VERB	_	Mood=Ind|Number=Sing|Tense=Pres|VerbForm=Fin	18	mod@relcl	_	Person[ctxt]=3|WordAlignmentBegin=365464|WordAlignmentEnd=365614
29	mettre	mettre	VERB	_	VerbForm=Inf	28	comp:obj	_	SpaceAfter=No|Subject=NoRaising|WordAlignmentBegin=365614|WordAlignmentEnd=365880
30	…	…	PUNCT	_	_	6	punct	_	WordAlignmentBegin=365880|WordAlignmentEnd=366116
</conll>

Note that the reparandum has been attached to its repair in the previous example, even if the result is non projective.

> [!note] Innstead of `reparandum`which goes from right to left, it would have been possible to use a relation, that would have been names `repair`, going from left to right, as `conj:reform`.
> But this may result in some problems, especially when the reparandum is incomplete or headed by a interrupted word.

> [!tips]
> For more examples on disfluencies, you can refer to the [disfluency](guidelines/universal/construction/disfluency) page.

