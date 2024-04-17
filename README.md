<center> <h1>Cheminformatic Analysis for Drug Discovery:</h1> </center>
 
<center> <h2>Looking for a Alzheimer's treatment.</h2> </center>

<center> <h3></h3> </center>

<center> <h5>Camila Gallo Chaubell, Pablo La Spina, Belen Maciel and Malena Tejerina Cibello</h5> </center>


<p>Cheminformatics project 2023
<p>Universidad Nacional de San Martin (National University of San Martin). Buenos Aires, Argentina.

<h3>Introduction</h3>

<p align="justify"> Alzheimer's disease (AD) is a neurodegenerative disease that causes progressive loss of memory, thinking ability, and cognitive skills. In most people, symptoms appear at an older age and this disease is the most common cause of the development of dementia [1,2]. At the molecular level, it is characterized by the accumulation and aggregation of extracellular plaques with β-amyloid (Aβ) peptides together with intracellular neurofibrillary tangles containing tau, a protein associated with microtubules, which prevents the passage of essential molecules and nutrients to the neuronal cells. This is associated with the loss of synaptic plasticity of neurons, axonal transport and, therefore, the loss of synapses and neurons [1,3].
<p align="justify"> AD refers to a pathological process that takes years to develop, while dementia refers to a late phase of it. Likewise, this disease usually begins in the absence of symptoms, so its early diagnosis is difficult and it is still not clear if all individuals progress to the development of dementia. It is very important to focus on the pathology prior to the onset of dementia since it will then be too late to recover the brain [2]. Currently, dementia risk reduction is one of the strategic action areas of the World Health Organization's global action plan on dementia [4].
<p align="justify"> Although this disease has no cure, different treatments based on the use of small chemical molecules and monoclonal antibodies have been developed and approved. On the other hand, in the dementia stage, existing treatments focus on slowing down the progression or appearance of symptoms [1,2]. The latest drugs approved by the FDA for the treatment of AD are monoclonal antibodies directed against the amyloid beta peptide, aducanumab and lecanemab [2]. Donepezil, rivastigmine, and galantamine are other oral drugs that have been approved to relieve symptoms of the disease. The latter are classified as inhibitors of the enzyme Acetylcholinesterase (AChE), which causes an increase in the availability of the neurotransmitter acetylcholine, enhancing the synapse and favoring the treatment of symptoms related to memory, thinking, language, among others [1,3,5].
<p align="justify"> The coumarin or Chromenone functional group (chembl_id: CHEMBL6466) is an aromatic organic chemical compound with a benzene molecule with two adjacent hydrogen atoms replaced by an unsaturated lactone ring, forming a second six-membered heterocycle that shares two carbons with the ring. of benzene (Fig. 1). It is a substance, present in certain plant species, used to make medications that prevent and treat blood clots in blood vessels, that is, it is a type of anticoagulant used for the treatment of heart conditions [6]. This group can be found in thousands of bioactive synthetic molecules since its unique and versatile oxygenated heterocyclic structure makes it a very good scaffold for substitutions or various chemical arrangements [3,6].

![Chromenona](https://github.com/camilachaubell/DrugDiscovery-Chromenone/blob/main/images/chromenone_functional_group.png?raw=true)

*Figure 1. Molecular structure of the coumarin or Chromenone functional group*

<p align="justify"> Regarding AD, it has been determined that molecules with a Chromenone nucleus have biological effects on several aspects of the disease, particularly in their potential to inhibit AChE. They are “anti-Alzheimer's” compounds that, through molecular docking, have been shown to simulate the natural substrate of the enzyme [3]. For this reason, in this work the chemoinformatic analysis of compounds with a percentage of structural similarity greater than 40% with Chromenone is proposed to determine their drug-type profile and, from this, propose feasible candidates to be acquired or synthesized and analyzed. a posteriori for the potential development of a new treatment against Alzheimer's disease.

<h3>Hypothesis</h3>
<p align="justify"> The cheminformatics analysis of chemical compounds containing the Chromenone functional group is a tool that allows the discovery of novel drugs to be used in the development of a new treatment against Alzheimer's disease.

<h3>Objetives</h3>
<h4>General Objective</h4>
<i>In silico</i> selection of drug-like chemical molecules containing the Chromenone functional group, candidates for the development of a new treatment against Alzheimer's disease.
<h4>Specific Objectives</h4>

1.   Collect from ChEMBL the molecules that have a similarity greater than 40% with Chromenone.
2.   Explore structural diversity by doing fingerprint clustering.
3.   Choose the best druggability criteria or criteria to select the candidates to treat the pathology.

<h4><i>Data Collection</i></h4>

<p align="justify"> Using RDkit, we first searched for compounds that have a similarity percentage greater than or equal to 40% with the Coumarin functional group, using the ChEMBL database. With the data obtained, a dataframe was created from which repeated compounds were filtered using Inchikey. Different columns were also added for the selection criteria to be considered later.

<h4><i>Clusterization</i></h4>

<p align="justify"> Using the data frame obtained in the previous step, the fingerprints for all the molecules were calculated. A table was generated to compare all the molecules based on their similarity, and a heatmap was made to visualize the data. For clustering, the linkage() function was used. The 'average', 'single' and 'complete' methods of the linkage function were used to calculate the similarity distance matrices between molecules. They were compared graphically using dendrograms and the 'linked complete' type of clustering was selected with a cut-off point or threshold of 2, which was used to graph a new dendrogram that allowed better visualization of the 7 clusters formed and subsequently generated.

<h4><i>Drugability Criteria</i></h4>

<p align="justify"> Using the obtained clusters, different filters were applied to reach the selection of candidates. In the first instance, it was sought that the compounds could cross the blood-brain barrier (BBB), a key aspect to be used as a treatment for Alzheimer's disease; As a second filter, Lipinski's rules were used to select compounds that can be administered orally and are of the drug type or druglikeness; The third filter applied was 'PAINS' to avoid very promiscuous molecules and false positives; The fourth filter used was that of Ghose, which considers criteria similar to Lipinski but with narrower margins. Finally, the use of the 'Brenk' filter that considers structural reactivity alerts was considered, but was ruled out for the final selection.

<h4><i>Candidate Selection</i></h4>

<p align="justify"> For the selection, those compounds that passed all the filters mentioned above and that are available for purchase at an affordable price were taken into account.
Additionally, those compounds whose 'synthetic accessibility score' is low were evaluated, their possibility of synthesis being high, that is, they are easy to produce. Finally, the structural similarity with reported acetylcholinesterase (AChE) inhibitors was also taken into account to select the best candidate(s).

<h3>Conclutions </h3>
<p align="justify">From the analysis carried out in this work, 44 compounds were selected that meet the minimum druggability criteria chosen to filter those that could potentially be used for a treatment against Alzheimer's disease. from among all those collected with a percentage of similarity greater than 40% with Chromenona. According to the urgency and/or availability to continue with the bioassays, priority has been given, on the one hand, to those compounds that are available for purchase and whose price is affordable, reducing the list of compounds to 12. On the other hand, of those 44 initially filtered, 12 compounds have also been selected (with representatives from all the clusters) whose synthetic accessibility score was good, that is, their synthesis would be easy to resort to another collaborator to carry it out.

<p align="justify">Additionally, the selection of the compound CHEMBL3742172 was proposed, which was filtered through substructure analysis due to similarity to AChE inhibitors as it has the structure that has been previously reported as a candidate to be stabilized within the enzymatic structure. [3].

<p align="justify">In summary, as a conclusion, it has been determined that the use of the cheminformatics tools learned allowed the selection of different chemical molecules, similar to drugs and with a functional Chromenone core, candidates to be tested in in vitro trials as a potential treatment for Alzheimer's disease.

<h3>References</h3>

[1] Alzheimer disease. Nat Rev Dis Primers 7, 34 (2021). https://doi.org/10.1038/s41572-021-00275-0

[2] Van der Flier, W.M., de Vugt, M.E., Smets, E.M.A. et al. Towards a future where Alzheimer’s disease pathology is stopped before the onset of dementia. Nat Aging 3, 494–505 (2023). https://doi.org/10.1038/s43587-023-00404-2

[3] Kamel N.N., Aly HF, Fouad G.I., Abd El-Karim S.S. et al. Anti-Alzheimer activity of new coumarin-based derivatives targeting acetylcholinesterase inhibition. RSC Adv. (2023). https://doi.org/10.1039/d3ra02344c  

[4] WHO. Global Status Report on the Public Health Response to Dementia. Report No. ISBN 978-92-4-003324-5 (World Health Organization, 2021).

[5] Colović MB, Krstić DZ, Lazarević-Pašti TD, Bondžić AM, Vasić VM. Acetylcholinesterase inhibitors: pharmacology and toxicology. Curr Neuropharmacol, 315-35 (2013). https://doi.org/10.2174/1570159X11311030006

[6] Matos MJ. Coumarin and Its Derivatives-Editorial. Molecules. (2021) https://doi.org/10.3390/molecules26206320

[7] Daina, A., Michielin, O. & Zoete, V. SwissADME: a free web tool to evaluate pharmacokinetics, drug-likeness and medicinal chemistry friendliness of small molecules. Sci Rep 7, 42717 (2017). https://doi.org/10.1038/srep42717

[8] Daina, A. & Zoete, V. A BOILED-Egg To Predict Gastrointestinal Absorption and Brain Penetration of Small Molecules. ChemMedChem (2016).  https://doi.org/10.1002/cmdc.201600182

[9] Lipinski, C.A. Lead- and drug-like compounds: the rule-of-five revolution. Drug Discovery Today: Technologies (2004). https://doi.org/10.1016/j.ddtec.2004.11.007.

[10] Arup K. Ghose, Vellarkad N. Viswanadhan, and John J. Wendoloski. A Knowledge-Based Approach in Designing Combinatorial or Medicinal Chemistry Libraries for Drug Discovery. J. Comb. Chem(1999). https://doi.org/10.1021/cc9800071.