# Fuzzy Logic | Introduction

- The term fuzzy refers to things that are not clear or are vague. In the real world many times we encounter a situation when we can’t determine whether the state is true or false, their fuzzy logic provides very valuable flexibility for reasoning. In this way, we can consider the inaccuracies and uncertainties of any situation. 

- In the boolean system truth value, 1.0 represents the absolute truth value and 0.0 represents the absolute false value. But in the fuzzy system, there is no logic for the absolute truth and absolute false value. But in fuzzy logic, there is an intermediate value too present which is partially true and partially false. 


# Architecture 

Its Architecture contains four parts :

- RULE BASE: It contains the set of rules and the IF-THEN conditions provided by the experts to govern the decision-making system, on the basis of linguistic information. Recent developments in fuzzy theory offer several effective methods for the design and tuning of fuzzy controllers. Most of these developments reduce the number of fuzzy rules.
- FUZZIFICATION: It is used to convert inputs i.e. crisp numbers into fuzzy sets. Crisp inputs are basically the exact inputs measured by sensors and passed into the control system for processing, such as temperature, pressure, rpm’s, etc.
- INFERENCE ENGINE: It determines the matching degree of the current fuzzy input with respect to each rule and decides which rules are to be fired according to the input field. Next, the fired rules are combined to form the control actions.
- DEFUZZIFICATION: It is used to convert the fuzzy sets obtained by the inference engine into a crisp value. There are several defuzzification methods available and the best-suited one is used with a specific expert system to reduce the error.


# Membership function

-  A graph that defines how each point in the input space is mapped to membership value between 0 and 1. Input space is often referred to as the universe of discourse or universal set (u), which contains all the possible elements of concern in each particular application. 

# There are largely three types of fuzzifiers:  

Singleton fuzzifier
Gaussian fuzzifier
Trapezoidal or triangular fuzzifier

# What is Fuzzy Control? 

It is a technique to embody human-like thinkings into a control system.
It may not be designed to give accurate reasoning but it is designed to give acceptable reasoning.
It can emulate human deductive thinking, that is, the process people use to infer conclusions from what they know.
Any uncertainties can be easily dealt with the help of fuzzy logic.
Advantages of Fuzzy Logic System 

This system can work with any type of inputs whether it is imprecise, distorted or noisy input information.
The construction of Fuzzy Logic Systems is easy and understandable.
Fuzzy logic comes with mathematical concepts of set theory and the reasoning of that is quite simple.
It provides a very efficient solution to complex problems in all fields of life as it resembles human reasoning and decision-making.
The algorithms can be described with little data, so little memory is required.
Disadvantages of Fuzzy Logic Systems 

Many researchers proposed different ways to solve a given problem through fuzzy logic which leads to ambiguity. There is no systematic approach to solve a given problem through fuzzy logic.
Proof of its characteristics is difficult or impossible in most cases because every time we do not get a mathematical description of our approach.
As fuzzy logic works on precise as well as imprecise data so most of the time accuracy is compromised.

# Application 

- It is used in the aerospace field for altitude control of spacecraft and satellites.
- It has been used in the automotive system for speed control, traffic control.
- It is used for decision-making support systems and personal evaluation in the large company business.
- It has application in the chemical industry for controlling the pH, drying, chemical distillation process.
- Fuzzy logic is used in Natural language processing and various intensive applications in Artificial Intelligence.
- Fuzzy logic is extensively used in modern control systems such as expert systems.
- Fuzzy Logic is used with Neural Networks as it mimics how a person would make decisions, only much faster.
- It is done by Aggregation of data and changing it into more meaningful data by forming partial truths as Fuzzy sets.



# What is Fuzzy Set ?

Fuzzy refers to something that is unclear or vague . Hence, Fuzzy Set is a Set where every key is associated with value, which is between 0 to 1 based on the certainity .This value is often called as degree of membership.
Fuzzy Set is denoted with a Tilde Sign on top of the normal Set notation.


# Operations on Fuzzy Sets-

1. Union :

Consider 2 Fuzzy Sets denoted by A and  B, then let’s consider Y be the Union of them, then for every member of  A and  B, Y will be:

 degree_of_membership(Y)= max(degree_of_membership(A), degree_of_membership(B)) 
 
 
 2. Intersection :

Consider 2 Fuzzy Sets denoted by A and  B, then let’s consider Y be the Intersection of them, then for every member of  A and  B, Y will be:

degree_of_membership(Y)= min(degree_of_membership(A), degree_of_membership(B)) 


3. Complement :

Consider a Fuzzy Sets denoted by A  , then let’s consider Y be the Complement of it, then for every member of  A  , Y will be:

degree_of_membership(Y)= 1 - degree_of_membership(A)


4. Difference :  
Consider 2 Fuzzy Sets denoted by A and  B, then let’s consider Y be the Intersection of them, then for every member of  A and  B, Y will be:

degree_of_membership(Y)= min(degree_of_membership(A), 1- degree_of_membership(B)) 




- Fuzzification:
It is the method of transforming a crisp quantity into a fuzzy quantity. This can be achieved by identifying the various known crisp and deterministic quantities as completely nondeterministic and quite uncertain in nature. This uncertainty may have emerged because of vagueness and imprecision which then lead the variables to be represented by a membership function as they cab be fuzzy in nature.

For example, when I say the temperature is 45° Celsius the viewer converts the crisp input value into a linguistic variable like favourable temperature for the human body, hot or cold.

- Defuzzification:
It is the inversion of fuzzification, there the mapping is done to convert the crisp results into fuzzy results but here the mapping is done to convert the fuzzy results into crisp results.
This process is capable of generating a nonfuzzy control action which illustrates the possibility distribution of an inferred fuzzy control action.

Defuzzification process can also be treated as the rounding off process, where fuzzy set having a group of membership values on the unit interval reduced to a single scalar quantity.

| Comparison | Fuzzification | Defuzzification |
| ----------- | ----------- |
| Basic | 	Precise data is converted into imprecise data. | Imprecise data is converted into precise data. |
| Definition | Fuzzification is the method of converting a crisp quantity into a fuzzy quantity. | Defuzzification is the inverse process of fuzzification where the mapping is done to convert the fuzzy results into crisp results. |
| Example | Like, Voltmeter | Stepper motor and D/A converter |
| Methods | Intuition, inference, rank ordering, angular fuzzy sets, neural network, etcetera.	 | Maximum membership principle, centroid method, weighted average method, center of sums, etcetera. |
| Complexity | It is quite simple. | It is quite complicated. |
| Use | It can use IF-THEN rules for fuzzifying the crisp value. | It uses the center of gravity methods to find the centroid of the sets.
 |







# DEFUZZIFICATION TECGNIQUES(http://vlabs.iitb.ac.in/vlabs-dev/labs/machine_learning/labs/exp9/theory.php)->

1)Lambda-Cut Method
2)Maxima Methods
  a)First of maxima(FOM)
  b)Last of maxima(LOM)
  c)Mean of Maxima(MOM)
3)Weighted Sum Method
4)Centroid Methods
  a)Center of Sum(COS)
  b)Center of Gravity(COG)

LAMBDA-CUT METHOD(easy)-> compare the value of membership value with given value of lambda. If it is greater or equal(>=) make it 1 else make it 0.
FIRST OF MAXIMA-> the first maximum value.
LAST OF MAXIMA-> the last maximum value
MEAN OF MAXIMA-> mean of the maximum values.
WEIGHTED AVERAGE METHOD->sumation of(element* membership value)/(sum of membership values)

CENTER OF SUM->sumation of(area of the component* center)/sumation of(area)

