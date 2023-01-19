Formal logic focuses on the relationship betweenstatements as opposed to the content of any particularstatement.

Applications of formal logic in computer science:
	Prolog: programming language based on logic.
	Circuit Logic: logic governing computer circuitry.

Definition of a statement:
	A statement, also called a proposition, is a sentence that iseither true or false, but not both.
	The truth value of a statement is T (1) or F (0).

An example to illustrate how logic really helps us, 3 statementswritten below: 
	All mathematicians wear sandals. 
	Anyone who wears sandals is an algebraist. 
	Therefore, all mathematicians are algebraists

Logic is of no help in determining the individual truth of thesestatements. However, if the first two statements are true, logic assures thetruth of the third statement. Logical methods are used in mathematics to prove theorems andin computer science to prove that programs do what they aresupposed to do.

Usually, letters like A, B, C, D, etc. are used to representstatements.
	Combining letters, connectives, and parentheses can generate an expression which is meaningful, called a wff.  
		(A --> B) V (B --> A) is a wff but A )) V B (--> C) is not

Logical connectives are symbols such as Λ, V, <-->, -->.
	Λ represents AND (Conjunction)	
	V represents OR (Disjunction)
	--> represents IMPLICATION
	<--> represents EQUIVALENCE
	´ represents NOT (Negation)

Truth Tables

The total number of rows in a truth table for n statement letters is 2pow(n)

	(A Λ B)
		A B (A Λ B)
		T T    T
		T F    F
		F T    F
		F F    F

	(A V B)
		A B (A V B)
		T T    T
		T F    T
		F T    T
		F F    F
	
	(A --> B)      <--->        A´ V B
		A B (A --> B)            A A´ B (A´ V B)
		T T     T                T F T      T 
		T F     F                T F F      F
		F T     T                F T T      T
		F F     T                F T F      T
	
	(A <--> B)
		A B (A <--> B)
		T T      T
		T F      F
		F T      F
		F F      T

	(A A´)
		(A A´)
		  T F
		  F T

Equivalences:
	Two statement forms are called logically equivalent if, and only if, they have identical truth values or each possible substitution of statements for their statement variables.
	The logical equivalence of statement forms P and Q is denoted  
	by writing P <--> Q or P ≡ Q.

Tautology definition:
	A wff that is intrinsically true, i.e. no matter what the truth value of the statements that comprise the wff.  Usually, tautology is represented by 1 
		It will rain today or it will not rain today ( A V A´ )  
		P <--> Q where P is A --> B and Q is A´ V B

Contradiction definition:  
	A wff that is intrinsically false, i.e. no matter what the truth value of the statements that comprise the wff.  Usually, contradiction is represented by 0 
		It will rain today and it will not rain today ( A Λ A´ )  
		(A Λ B) Λ A´

Some Common Equivalences
	Commutative: A V B <--> B V A                             A Λ B <--> B Λ A  
	Associative:     (A V B) V C <--> A V (B V C)           (A Λ B) Λ C <--> A Λ (B Λ C)  
	Distributive:    A V (B Λ C) <--> (A V B) Λ (A V C)   A Λ (B V C) <--> (A Λ B) V (A Λ C)  
	Identity:          A V 0 <--> A                                    A Λ 1 <--> A  
	Complement: A V A´ <-->  1                                  A Λ A´ <--> 0

De Morgan’s Laws
	(A V B)´ <--> A´ Λ B´	
	(A Λ B)´ <--> A´ V B´