# CinC 2020 Presentation [here](https://github.com/lucasabdalah/I3S-Internship/blob/master/CinC%202020/Presentation/CinC2020.pdf)

Relevants points of the presentation:

## Short Explanation about the subject (1/17)
    1) I'm Lucas de S. Abdalah and i'm undergraduted student at Universidade Federal do Ceara, Fortaleza, Brazi.
    2) I'm glad to present our work today, named: Tensor-Based noninvase AF Complexity Index For CA. 
    3) This presentation is result of my internship at I3S laboratory during a year of exchange at Universite Cote d'Azur. 
    4) In this work, we propose a new AF complexity index based on tensor decomposition as a potential tool to help guide CA.

## AF (2/17)
    1) is the most common sustained cardiac arrhythmia in clinical practice.
    2) In the European Union, 8.8 million adults over 55 years had AF in 2010. Is projected that this number will double by 2060 to 17.9 million. 
    3) Howver, the complex physiological processes associated that leads to AF, are complex and not completely understood.
    4) This a challenging cardiac condition known as the last great frontier in cardiac electrophysiology.
        
## Step-wise CA (3/17)
    1) Existing drugs and surgical therapies are widely used aiming to mitigate AF symptoms, and their use depend on medical preescription/indication.
    2) Step-wise CA is one of them, an effective therapy to treat persistent AF and restore sinus rhythm.
    3) Its use implicates a catheter incision to scar regions thought to be responsible by triggering the fibrillation.
    4) Noninvase methods can help locate the sources, as well as measure the complexity and consequently the impact, for example of PVI and other widely used techniques.
    
## Matrix Approach (4/17)
    1) Signal Processing Techniques to assess noninvasevely 
    2) VA and AA are sumed uncopled, the problem admits BBS formulation
    1) To estimate these sources, the ECG data matrix can be modeled, 
    2) Constraints: Limited Rank, Orthogonality, Statistical Independence. May lack physiological background.
    3) Tensor Approach under much milder Constraints.

## Tensor Approach (5/17)
    1) A tensor is an extesion of the concept of matrix. Square with number spread through a 2D structure.A 3rd-order tensor as a cube filled with numbers, a 3D structure. A collection of matrices in the depth dimension.
    2) Tensor decompositions are mathematical operations that aim to factorize this data as a sum of simpler tensor.
    3) BTD based on Hankel structure.
    4) These decompostions have celebrated results in telecomunications and biomedical fields, with a lot of applications.

## BTD-Hankel Model (6/17)
    1) AF signal represented by an all-pole model, i.e, sum of complex exponentials.
    2) AA signal quasi periodic characteristic allows mapping the signal as a structured Hankel matrix.
    3) That consists in taking each sample of an ECG-lead and placing it at the matrix anti-diagonal (as shown in the Figure).
    4) This mapping allows to know the number of poles contained in the signal, since the matrix rank is equal to these number of poles.
    
## Tensor Approach (7/17)
    1) Repeat the process for each lead.
    2) Then stack this matrices in a 3rd-order tensor (Y).

## BTD Approach (8/17)
    1) Challenge of parameter estimation

## CAGL (9/17)
    1) Classical BTD Approach
        * Fixed structured.
        * Minize the function f - Euclidian distance.
        * Prior knowledge of the structure (R,Lr).

    2) CAGL Approach
        * Is a recently prosed algorithm to compute BTD with Hankel structure ensured at each iteration.
        * Non fixed structure mixing the classical approach.
        * Penalization term and function g limiting the structure and number of blocks.
        * Estimation of the model parameters (R,Lr).

## AF Complexity Index (10/17)
    1) More poles, more complex it can be considered.
    2) The proposed index consists in assess the AA Hankel Matrix Rank.

## AA Source Classification (11/17)
    1) AA source classification still a problem. 
    2) SC, DF, kurtosis and visual inspection to evaluate the AA extraction.
    3) The source that maximize SC or kurtosis (A high kurtosis is thus suggestive of a harmonic signal like AA signal during AF)

## AA Source Estimation (12/17)
    1) This an example of AA signal estimation (red - dashed line) and the lead V1 (blue line).
    2) Presenting rank 33 and the value parameters.

## Database and Experimental setup (13/17)
    1) 20 patients suffering from persistent.
    2) 59 ECG segments
    3) Very short segments (Heartbeat0)
    4) Largest TQ segment.
    5) Monaco.

## CA impact to Atrial Activity Complexity (14/17)
    1) Box-and-whisker plot showing the proposed index for each CA step.
    2) Labels. 
    3) One can see that, as the CA is performed, that such index decreases.

## PVI impact (15/17)
    1) Box-and-whisker plot showing the proposed index for 17 patients undergoing PVI.

## AF recurrence and complexity (16/17)
    1) An interesting assessment is a relevant statistical correlation (Pearson) for 18 followed patients.
    2) AF recurrence, i.e, the time to the patient present new episodes of AF.
    3) The index measured before the CA procedure.

## Conclusion (17/17)
    1) Contributions
    * CAGL is able to jointly extract the AA signal from the ECG and measure AF complexity
    * Very short recordings. (1.06 $\pm$ 0.20 s)
    * Validation in 20 patients undergoing CA.
	    - Expected decreasing AF complexity throughout CA steps
		- Significant correlation with AF recurrence after CA
    2) Clinical Impact
    * Help guide CA in real time
    3) Future Work
    * Increase the database 
    * Compare with other state-of-the-art indices.
