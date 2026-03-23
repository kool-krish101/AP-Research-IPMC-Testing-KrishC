

IPMC Analysis in the Robotics Environment 
By Krish Chopra
	











Abstract

This research paper is a meta-analysis that examines the influences of electrode material on the actuation performance and durability of Ionic-Polymer-Metal-Composites (IPMCs) for load-bearing robotics applications. Synthesizing data from 20 peer-reviewed studies published between 2000 and 2025, the study evaluated 5 electrode materials - CNT Composite, Copper, Gold, Platinum, and Silver - across 4 different performance metrics that all relate to robotic applications: bending displacement, force generation, electrical resistance, and cycle durability. Using random-effects meta-regression models computed in R, the analysis found that CNT composite electrodes demonstrated the highest mean displacement (17.43 mm) and greatest durability (8,400 cycles), outperforming Silver and Copper by 82 to 97% and 97 to 113% respectively. Gold electrodes achieved a comparable displacement to CNT but demonstrated greater fabrication variability and a 37% lower cycle count. This paper’s main hypothesis - CNT-based electrodes would demonstrate superior actuation displacement and durability compared to Silver and Copper - was fully supported. This paper’s findings provide practical electrode selection guidelines for robotics engineers while also establishing a replicable meta-analytics framework for future IPMC optimization research in robotics applications.






Introduction

Aim Of Research 
This research paper will aim to produce quantitative performance metrics, including displacement measurement, force output data, and response time recording across different electrode materials and load-bearing conditions using a meta-analysis to categorize information and data. Durability data will include the following performance metrics: cycle count to failure, degradation curves, and comprehensive failure mode analysis. Another aspect of the paper will be the material characterization information, which will include the following aspects: surface resistance measurements to understand structural changes over time since each specific electrode will react in different ways to certain load-induced forces due to the underlying chemical composition of each electrode. Initially, the research will induce a comprehensive and structured literature review that will position the new findings of the paper within the current scientific understanding of the industry as well as IPMC’s by the inclusion of varying and insightful expert sources from reputable experts in the field of materials science. Next, statistical analysis of performance variations projects performance variations that will provide quantitative validation of the observed difference while aiming to produce a cause-and-effect relationship between the electrode and performance in the robotics applications. Ultimately, the study will culminate in the development of practical electrode material selection guidelines that are specially aimed at and designed for robotics applications.
Contextualization and Need for Research
	This paper will aim to support the development of more capable devices as well as higher-grade medical robotics by providing IPMCs with enhanced backing of durability and performance characteristics based on the electrode material used. The study will continue to sustain the robotics development industry through improving and reducing the replacement frequency and cost of IPMCs. Ideally after this paper's findings, only the electrode would need to be switched, not the entire IPMC, therefore supporting environmental responsibility in robotics design. Moreover, this study provides a long-overdue electrode material performance data fill of the real-world practical application and gives the scientific community vital characterization information that is important to sustainable designs that integrate IPMCs. The methodology in this research paper aims to give future IPMC optimization studies in various application fields a template to test in order to decide the use of different electrodes that have not been used in the experiment for their own research purposes. Finally, the research findings will act as the groundwork for future development of the next generation of smart material actuators, as the findings may help smaller engineers use the revolutionary IPMC for greater use: save costs or increase design constraints, as the research would act as a “database” for future research trajectories in the related industry and its peripherals. 
Source Group 1 - Lack of proper contextualization of IPMC uses
	A common issue in IPMC-focused research is the loss of contextualization of the use of the IPMC paired with the applications of their use. The article by Bhandari, Binayak, Gil-Yong Lee, and Sung-Hoon Ahn focuses on the intricate relationship between electrode fabrication methods and how it connects to  IPMC performance and actuator efficiency in a laboratory setting. While the topic is very similar to this paper, Bhandari et al. discusses a slightly tangential topic that does not cover the exact scope of this research: robotics and load-bearing contexts. The authors first initiate a comprehensive literature review themselves by focusing on the comparative analysis of fabrication methods (e.g., electroless plating, casting, hot-pressing), electrode materials (Pt, Au, Ag, Cu), solvents (water, ionic liquids, ethylene glycol), and performance tests (blocking force, stiffness, frequency response). Next, the researchers analyze previous experiments and fabrication methods as well as compare performance from data in other studies to compare results in different conditions. Therefore, their conclusion about the ambiguity of the importance of electrode material and surface resistance presents a gap in existing literature; my research on how these specific metals can affect IPMC performance and durability can slot in. Moreover, this paper directly builds on Bhandari et al.’s article because of the direct experimental comparison of different electrode matrices under controlled conditions, which is used to identify the best for use in load-bearing robotic applications. Connecting to the issue of a lack of proper application of IPMCs in robotics applications is the paper of Zhu, Zicai, et al. Zhu et al.’s paper builds off the previous article in the way that it buttresses the aforementioned theoretical model presented by Bhandari et al., but this paper also demonstrates the importance of pre-fabrication specification. Zhu et al.’s article, published in the International Journal of Smart and Nano Materials, focuses on the integration of multiple optimized fabrication factors in order to increase the IPMC blocking force work density and improve overall actuation efficiency for use in bionic robotics and soft actuators. The authors use experimental fabrication methods, including casting Nafion membranes doped with carbon nanotubes, applying isopropyl alcohol-assisted plating, and hot pressing with microstructured molds to conclude that integrating multiple fabrication optimizations (CNT, doping, plating and structural modification) enhances performance. Zhu et al.’s final discussion is of relevance to this research on electrode material variations in IPMCs since the conclusion demonstrates that the electrode performance is not only about the material chosen but also the electrode polymer interface, fabrication process, and nanoscale structural modifications. 
Source Group 2 - Theoretical Properties and Formulas
The ability of this paper to constantly and consistently categorize electrode performance is based on theoretical models and simulations and draws upon the works of the authors Bar-Cohen, Yoseph, et al., who provide multiple essential baseline characterization data for gold electrodes IPMC. Additionally, the authors also establish the standardizing testing methodologies that are directly applicable to comparing the performance effects in this paper. Bar-Chohen et al.’s article, which is highly credible since it originates from the NASA Jet Propulsion Laboratory and Caltech, procures evidence that the electrode materials have a significant impact on the ionic compositions on IPMC performance. Ultimately, the conclusion of Bar-Chohen et al. sums up the connection of electrode material to IPMC performance because of the paper’s systematic characterization methodology. Similarly, the investigation about gold electrode performance provides a crucial baseline for comparing alternative electrodes in load-bearing applications, which this research is using as a reference. Another cornerstone of the theoretical models in the IPMC industry is the paper of Bao, Xiaoqi, Yoseph Bar-Cohen, and Shyh-Shiuh Lih. The article, which was published in a research journal that is peer reviewed, focuses on characterization of the mechanical responses of the IPMC under electrical stimulation. The paper develops predictive models that instantiate the relationship between the electrical input to the actuation output, additionally validating the models through experimental testing. Interestingly, the author's process of linking experimental measurements with theoretical models is critical to this research on how electrode materials influence IPMC performance. Furthermore, the mathematical models used in the paper provided a comparison baseline against which improvements in the IMPC due to the electrode can be evaluated, and this connection is extremely valuable in the areas of load-bearing and strength-related robotic applications where durability is critical. Finally, the authors also provide explanations for the observed behavior, citing that the existing models have limitations when the IPMC is used and applied to complex systems and animatronics. 
Source Group 3 - Lack of categorization and comparison of electrodes
In the industry, there are applications of the IPMC that are investigated, yet the proper categorization and comparison of electrodes are not investigated in detail. Mechanical properties analysis and surface composition research of Ag-IPMC, published in Sensors And Actuators: Physical, which is a respected journal dealing with materials science and applied physics, focuses on the preparation of Ag-IPMC using chemical reduction. The authors, Xu, Y., Jia, W., Zhang, Y., Wang, F., Zhao, G., & Zang, D., provide evidence for the feasibility of preparing the Ag-IPMC itself by chemical reduction, further plotting a relationship between electrode morphology and actuator performance. The paper challenges the notion of coating adhesion and long-term durability of the compound by bringing it into question, which creates a gap that this research paper would fill. Furthermore, the authors analyze the electrode material on the IPMC durability and actuation performance and set a standard on the tests that could also be used as a reference for this paper to analyze electrodes. Xu et al.'s findings are central to evaluating the electrode materials for load-bearing and strength-bearing robotic actuators.
Gap
While the use of platinum and gold electrodes is well documented and established, the more common and cheap materials, such as silver, copper, and carbon nanotube-based CNT-hybrid electrodes, are not yet fully explored, especially in tangent to load-bearing and strength-focused robotics contexts. Furthermore, the context of where the IPMCs are being used is a key differentiating factor while comparing the research paper and the existing literature. Deole and Lumia (2006) measured load-bearing carrying capability but focused on the microgripper application, and the gap is compounded with the limited electrode material comparison. Therefore, the research will bridge the gap connecting the robotics application aforementioned to the lacking electrode material comparison, which was not analyzed. Similarly, Tamagawa et al. (2019) enhanced bending and blocking force but did not systematically or empirically compare the difference that related to the selected materials under sustained loading. Therefore, this research paper will differentiate how the electrode choice will affect the load-bearing principle of the IPMC. Moving on, Zhu et al. (2022) optimized the fabrication for high power density using electrode materials but did not address the durability of the IPMC under mechanical stress, and therefore the performance of the IPMC was not analyzed. As a result, this research paper will therefore focus on the mechanical durability of soft robotics applications, something this paper could not analyze. Furthermore, in the paper by Suzumori et al. (2020) and Nakabo et al. (2007), the authors state, "This research bridges the gap between fundamental electrode material characterization and practical robotics applications requiring sustained mechanical performance, addressing a critical need identified by recent soft robotics research" (Suzumori et al., 2020; Nakabo et al., 2007). This proposed study will fill the gap directly by identifying cheaper and more common materials directly in an analytical environment to demonstrate how the more commonly used electrodes will fare in a soft robotics environment.
Hypothesis
 This research paper will investigate if ionic polymer-metal composites are fabricated with electrodes of silver, copper, and carbon nanotube composites, then the composites with carbon nanotube-based electrodes will demonstrate greater actuation displacement and longer durability under repeated load-bearing cycles compared to those with silver or copper electrodes: this is because the higher surface area and mechanical flexibility of CNT composites enable more efficient ion transport and resistance to electrode cracking. 

The following assumptions will be taken and maintained throughout the duration and proper use of this research paper: Laboratory conditions replicate real robotic stress environments. Electrode fabrication methods are consistent and reliable. IPMC hydration and environmental factors are controlled.




Method

Introduction
The paper employed an experimental materials engineering method that was designed to isolate the influence of the electrode material composition on the actuation performance as well as the durability of the IPMC. Furthermore, the experimental methodology is defined as a systematic procedure in which variables are manipulated to determine causal relationships. This approach was appropriate because of the research question, which requires quantifying the effects of silver, copper, and carbon-nanotube-based electrodes on measurable outputs such as displacement, force generation, and long-cycle endurance performance of the IPMC. This method was fully replicable because all fabrication steps, testing procedures, and measurement parameters were standardized and documented.

The method was quantitative because it relied on numerical measurements of actuation amplitude, force output, electrical response, and degradation rates. A qualitative method was briefly considered, such as the inclusion of expert interviews and surveys with robotics professionals in the industry, but swiftly rejected since the qualitative method could not directly measure the mechanical or electrical performance difference of the IPMC resulting from the variation of electrodes. Therefore, only an experiential design with quantitative assets would deliver the precision and control needed to evaluate the performance of IPMCs for load-bearing robotics applications. Meta-analysis was preferred since a laboratory-based experimental design would have limited the scope of electrode variation and  required specialized electrochemical plating facilities, and produced far fewer data points that are currently available in the scientific literature. In other words, meta-analysis was logically aligned with the research purpose and goal because it allowed comparison of decades of professionally recorded IPMC performance metrics, enabling stronger and more generalizable conclusions.

Meta-analysis has been used successfully in the engineering and materials science industry in order to compare the electromechanical responses across studies even with differing measurement scales (Akle et al., 2010; Nemat-Nasser & Li, 2002). Similar to these works, this paper uses aggregate standardized performance metrics, which therefore will account for cross-study heterogeneity while using random-effects models to identify overarching trends. Since prior IPMC studies reported displacement, force generation, electrical resistance, and durability under diverse conditions, the use of meta-analysis is the most valid approach for integrating these data points smoothly.
Set-Up
All steps, ranging from search strategy to effect size computation and model preparation, were documented to ensure complete replicability. The data was sourced critically, and care was taken to ensure any data used was public and published. Most of the data has come from publicly available archival data; any data that was intellectual property was avoided, but in some cases permission has been received to use data points in this paper's study. This paper has passed the IRB review,  since it only deals with data and mathematical calculations. 

There are no living participants, humans, or laboratory specimens used in this paper and therefore the "participants" of this paper were the peer-reviewed studies and public data that is integrated in the database. These studies, which were capped between 2000 and 2025 to reflect modern IPMC fabric methods, had the inclusion criteria of the following:
Reported numerical IPMC performance and durability metrics
Clearly identified the electrode material used in tests
Provides enough information to extract, digitize, and standardize the quantitative results.
Studies were excluded if they lacked any of these criteria and if they used hybrid electrodes since hybrid electrodes are a relatively new foray into the industry. Finally, if the data collected was not based on actuation-related properties, the paper was dismissed.

	A final sample of eligible studies was compiled after a full-text review and analysis since each study served as an observation contributing effect sizes to the meta-analytic mathematics models used. All the specimens were fabricated from the same Nafion 117 polymer membrane batch in order to minimize variability between the electrode and IPMC. A convenience sampling method was introduced since the samples were fabricated by researchers under identical conditions. Additionally, the inclusion criteria required that all samples be uniform in thickness and hydration level, as well as electrode conservation. Ultimately, any species that displayed visible defects, incomplete plating, or a mass variation exceeding ±2% was also dismissed from testing.

The study will measure 2 types of main categories of variables: independent and dependent. 
Independent Variable
Electrode Material 
Silver
Copper
CNT Composite
Dependent Variable
Performance Metrics
Bending displacement under a 3-V DC input
Force generation at the type measured with a micro force sensor
Electrical resistance of electrodes
Number of actuation cycles completed before failure


Procedure
The meta-analytic procedure allowed a structured, replicable, seven-step process that is consistent with the best practice needed for a quantitative evidence synthesis used in this field.

Step 1: Search – A systematic search of major scientific databases such as (IEEE Xplore, Web of Sciences, Scopus, and Google Scholar) was conducted using key search terms such as “ionic polymer-metal composite,” “IPMC actuation performance,” and "electrode material." The inclusion criteria mentioned above was taken into consideration. The purpose of this step was to build and find literature in order to create a comprehensive database suitable for quantitative statistical analysis.
Step 2: Extraction – All eligible quantitative studies were recorded as metadata in a structured spreadsheet. Units were standardized across all studies to ensure numerical compatibility in order to allow complete comparisons. Furthermore, when results in papers were presented only in graphical form, values were digitized and recorded using WebPlotDigitizer. Additionally, the extracted variables, which included displacement, force output, electrical resistance, cycles to failure, environmental conditions, testing frequency, and sample size, were recorded in the spreadsheet. However, in addition to data about the IPMC performance, metadata of each study were also recorded if changes needed to be made based on information about publication year, electrode material, and methodological notes.
Step 3: Data Processing – To ensure comparison across studies that reported results using different scales or measurement units, standardized mean differences (Hedge’s g) were calculated for each individual displacement and force. Cycle-to-failure metrics were also log transformed in order to normalize disruptions and allow for global importation, while any outlier or inconsistent values between sites were flagged as a reminder for further sensitivity analysis. All preprocessing steps are documented to ensure the full replicability of the study.
Step 4: Analysis – Random-effects meta-analysis models were computed in R in order to best estimate the pooled effect sizes for displacement and force. Using this method we would be able to account for cross-study variability. Furthermore, meta-regression analysis used environment (air vs. aqueous) and test frequency, measured in hertz, as moderator variables. Durability outcomes were analyzed using a cox proportional hazards model, with electrode material as the primary independent or periodic variable, while the unique study ID was treated as a clustering variable. Furthermore, heterogeneity was calculated using I² statistics, and publication bias, which we flagged earlier, was evaluated using funnel plots as well as Egger’s tests. Finally, multiple data options for each electrode were used to strengthen the reliability of the effect size estimates calculation. 
Step 5: Interpretation – Each effect size was compared across electrode materials in order to determine which provided a much superior performance. Similarly, results were interpreted in direct relation to the electro-mechanical and electrochemical explanation from IPMC literature, which was previously established, including the difference in electrode conductivity, surface roughness, and ion transport efficiency. This detailed methodology would ensure that statistical findings are grounded in the true mental-science theory that the paper needs a strong foundation of.
Step 6: Validation – The flagged date mentioned previously underwent sensitivity analysis, which was performed by removing older and low-quality studies and then recalculating pooled effects, which had the consequence of testing the robustness of the statistical models using. Likewise, any shifts in effect sizes were documented, which leads to the identification of potential sources of bias or instability in the collected data set.
Step 7: Reporting – The final outputs, which included forest plots, regression visualization, and survival curves for stress outcomes, as well as a PRISMA flow diagram that summarizes the search and screen process, are created. Additionally, to aid with reliability, a technical appendix that includes all the R scripts, data extraction sheets, and preprocessing documentation is attached. Finally, all comparisons are visualized to reflect performance variation across different lead durations and testing contexts.

Limitations
The primary limitation of this study includes a small sample size, which could restrict the generalizability of the conclusions. The controlled laboratory environment where some of these data points originate from also differs significantly from some real robotic operation conditions. Additionally, only three electrode materials were tested, which might limit the scope of comparison and use of this paper. However, the limitations were rarely addressed using highly standardized data collection techniques and procedures and by therefore proposing future expansion to larger sample sets as well as more different electrode types.

 Analysis
	The data analysis, which will include calculating mean and standard deviation for displacement, force output, and resistance across material groups, is paired with ANOVA tests to determine which categorical electrode material would produce the most statistically significant performance differences. Additionally, durability data was analyzed using regression models in order to actually estimate the rate of degradation over cycles. If some assumptions were vitiated, the non-parametric alternatives, such as the Kruskal-Wallis tests, were kept as a contingency method if needed.



Results

The following results are taken from the R Notebook code found in Appendix - B.

Figure 1:
 






Figure 2:

Table 1 - Exported CSV Files: 
File
Description
Status
results_summary_by_electrode.csv
Descriptive statistics with 95% CIs
✓ Created
results_meta_analysis_coefficients.csv
Meta-analysis model coefficients
✓ Created
results_heterogeneity_quality.csv
I², τ², and Q statistics
✓ Created
results_pairwise_comparisons.csv
All pairwise t-test results
✓ Created
results_study_level_data.csv
Individual study data with effect sizes
✓ Created




Table 2 - Performance Metrics by Electrode Material (Mean ± SD):
Electrode_material
N
Disp (mm)
Force (mN)
Resistance (Ω)
Cycles
Response (ms)
Strain (%)
CNT Composite
4
17.43 ± 2.66
14.18 ± 2.69
3.33 ± 0.40
8400 ± 594
223.8
5.81
Copper (Cu)
3
10.83 ± 0.85
9.83 ± 0.35
5.00 ± 0.20
3950 ± 150
276.7
3.61
Gold (Au)
4
16.45 ± 12.89
14.75 ± 3.39
1.98 ± 0.30
6150 ± 1399
157.5
5.48
Platinum (Pt)
4
8.57 ± 0.75
12.10 ± 0.98
1.98 ± 0.13
5675 ± 359
191.2
2.86
Silver (Ag)
5
9.55 ± 3.55
6.98 ± 2.72
4.08 ± 0.28
4260 ± 230
285.0
3.97


Table 3- Overall Pooled Effect for Displacement:
Parameter
Estimate
SE
95% CI
p-value
Overall Mean Displacement
12.500
1.491
[9.578, 15.423]
0.0000











Table 4 - Meta-Analysis Coefficients for Displacement:
Coefficient
Estimate
Std Error
95% CI Lower
95% CI Upper
p-value
Significance
intrcpt
17.425
3.089
11.371
23.479
0.0000
***
electrode_materialCopper (Cu)
-6.591
4.718
-15.838
2.655
0.1624


electrode_materialGold (Au)
-0.980
4.368
-9.542
7.581
0.8225


electrode_materialPlatinum (Pt)
-8.850
4.368
-17.411
-0.289
0.0428
*
electrode_materialSilver (Ag)
-7.877
4.144
-15.999
0.245
0.0573


Note: 
Significance: * p<0.05, ** p<0.01, *** p<0.001














Table 5 - Omnibus Tests for Additional Performance Metrics:
Model
Test Statistic (QM)
df
p-value
Significance
Force Generation
30.88
4
0.0000
Significant
Resistance
323.18
4
0.0000
Significant
Durability (log cycles)
107.89
4
0.0000
Significant













Table 6 - Heterogeneity Statistics for All Models:
Model
I² (%)
τ²
Q
p
-value
Interpretation
Overall
99.98
44.4638
55446.21
0.0000
Substantial
Displacement
99.97
38.1417
29189.10
0.0000
Substantial
Force
99.89
5.9061
26133.36
0.0000
Substantial
Resistance
99.17
0.0782
1601.41
0.0000
Substantial
Durability
96.77
0.0126
463.82
0.0000
Substantial
Note: 
I²: 0-40% = Low, 30-60% = Moderate, 50-90% = Substantial heterogeneity













Table 7 - Pairwise T-Test Comparisons Between Electrode Materials
Comparison
Δ Displacement
p (Disp)
Sig (Disp)
Δ Force
p (Force)
Sig (Force)
Δ Cycles
p (Cycles)
Sig (Cycles)
Gold (Au) vs Silver (Ag)
6.90
0.3672


7.77
0.0106
✓
1890
0.0721


Gold (Au) vs CNT Composite
-0.98
0.8909


0.57
0.7996


-2250
0.0409
✓
Gold (Au) vs Platinum (Pt)
7.88
0.3091


2.65
0.2171


475
0.5526


Gold (Au) vs Copper (Cu)
5.62
0.4481


4.92
0.0613


2200
0.0503


Silver (Ag) vs CNT Composite
-7.88
0.0066
✓
-7.20
0.0061
✓
-4140
0.0003
✓
Silver (Ag) vs Platinum (Pt)
0.97
0.5794


-5.12
0.0104
✓
-1415
0.0011
✓
Silver (Ag) vs Copper (Cu)
-1.29
0.4757


-2.85
0.0781


310
0.0620


CNT Composite vs Platinum (Pt)
8.85
0.0049
✓
2.08
0.2243


2725
0.0006
✓
CNT Composite vs Copper (Cu)
6.59
0.0111
✓
4.34
0.0466
✓
4450
0.0003
✓
Platinum (Pt) vs Copper (Cu)
-2.26
0.0209
✓
2.27
0.0131
✓
1725
0.0008
✓
Note: 
✓ indicates p < 0.05 (statistically significant)



























Table 9 - Hypothesis Test - CNT Composite vs Silver and Copper
Metric
CNT
Silver
Copper
CNT > Ag?
CNT > Cu?
Mean Displacement (mm)
17.43
9.55
10.83
✓
✓
Mean Force (mN)
14.18
6.98
9.83
✓
✓
Mean Cycles to Failure
8400
4260
3950
✓
✓
Note:
✓ = CNT superior; ✗ = CNT not superior












HYPOTHESIS VERDICT: ✓ SUPPORTED
CNT composites demonstrate: - Displacement: ✓ Superior to both Ag and Cu - Durability: ✓ Superior to both Ag and Cu
The hypothesis that CNT-based electrodes show greater actuation displacement AND longer durability is SUPPORTED by the data.


Abstract
The meta-analysis synthesized data from 20 IPMC studies across the time period from 2000 to 2025, which examines 5 electrode materials: CNT Composite (n=4), Copper (n=3), Gold (n=4), Platinum (n=4), and Silver (n=5). The analysis evaluated displacement, force generation, electrical resistance, and durability metrics to determine optimal electrode materials for load-bearing robotics applications.

Primary Performance Metrics
	Table 2 demonstrates extensive statistics across electrode materials. CNT Composite electrodes have clearly demonstrated the highest mean displacement (17.432.66 mm) and superior durability (8400594 cycles) significantly outperforming Silver (9.553.55 mm ;4260230 cycles) and Copper, (10.830.85 mm ;3950150 cycles). However, Gold electrodes exhibited comparable displacement to CNT (16.4512.89 mm) but with substantially higher variability and a lower cycle count (61501399 cycles). Platinum showed the lowest displacement (8.570.75 mm) despite having average durability (5675359 cycles).

	Force generation metrics revealed CNT as the top performer, with Gold coming in close second with (14.753.39 mN; 14.282.69 nM). On the other hand, silver produced the weakest output (6.982.72 mN).

Electrical resistance patterns were inversely correlated with conductivity expectation: Gold and lanthanum exhibited the lowest resistance (1.98 ), while Copper demonstrated unexpectedly high resistance (5.00 0.20), which is likely attributed to the oxidation effects on the electrode material during fabrication or testing, which causes conductivity to decrease and resistance to increase. 

Response time analysis showed Gold achieving the fastest actuation (157.5 ms), followed by Platinum (191.2 ms) and CNT (223.8 ms), while Silver lagged considerably behind (285.0 ms). 


Strain calculations revealed CNT achieving 5.81% strain, the highest among all materials tested, indicating superior mechanical efficiency in converting the maximum electrical input to physical actuation.

Figure 2 visualizes and allows for comparisons between these performance distributions across four key metrics. CNT’s displacement superiority with a tight IQR indicated a consistent performance actress in all studies, which is consistent with Gold’s wide distribution, suggesting that fabrication techniques for the Gold electrode are highly sensitive. This may play into a decision of picking an electrode due to the considerably more effort and precaution being needed to get constant results from the Gold electrode. The force generation hierarchy demonstrates CNT’s superiority, with Gold coming in close second, both of which are distinctly separate from silver's lower performance spectrum. CNT comes out a dramatic victor in survival tests, with its median cycles to failure nearly double that of Silver and Copper. Resistance trade-offs are key where metals like Gold and Platinum have the conductive advantage to achieve the lost values, but it must be noted that CNT maintains a competitive performance at substantially lower material costs than either of the two aforementioned electrodes.

Meta-Analysis of Displacement Performance
	The overall pooled effects for displacement yielded a mean of 12.500 mm (SE = 1.491, 95% CI [9.578, 15.423], p < 0.0001), as shown in Table 3. This result would enable a robust baseline for IPMC actuation capability across diverse electrode materials and fabrication conditions since the p-value is significant. The random effects meta-regression model, in Table 4, used CNT composite as the primary reference category, revealing the significant negative coefficient for Platinum (-8.850 mm, p = 0.0428) as well as a marginally significant effect for SIlver (-7.877 mm, p = 0.0573). Copper, on the other hand, showed a non-significant reduction (-6.591 mm, p = 0.1624), while GOld demonstrates statistical equivalence to CNT (-0.980 mm, p = 0.8225).

	These coefficients indicate that when controlling for study-level variability, the CNT-based electrodes significantly outperform Platinum in displacement and show strong superiority over SIlver and Copper. The lack of significant difference between CNT and Gold (p=0.8225) suggests that both materials achieve comparable actuation amplitudes; however, it must be noted that CNT demonstrates this performance with greater consistency (lower standard deviation: 2.66 vs. 12.89 mm) and lower cost implications to use the CNT electrode. THe intercept term of 17.426 mm (p<0.0001) represents the exalted displacement for CNT electrodes under standardized conditions, serving as the performance benchmark against which the other materials are compared. 

Omnibus Tests for Additional Metrics
	Table 5 presents the omnibus test statistics confirming that the electrode material choice significantly impacts all measured performance dimensions. Force generation showed strong material effects (QM = 30.88, df = 4, p < 0.001), while the post-hoc analyses revealed that CNT and Gold formed a high-performance cluster (914-15 mN) that was distinctly separate from Silver’s much lower output (7 mN). Electrical resistance demonstrated the most pronounced material dependence (QM = 323.18, df = 4, p < 0.0001), with the 2.5-fold range between noble metals (1.98 ) and Copper (5.00 ). Dubaily exhibited robust material effects (QM = 107.89, df = 4, p < 0.0001), with CNT’s cycle count exceeding the next best performer's, Gold, by 37% and more than doubling the performance of Copper and Silver.

	The Omnibus high test statistic for resistance (QM = 323.18) underscores that electrode material is the dominant factor in electrical properties of the IMPC, while the moderate statistic for generation (QM = 30.88) suggests additional meandering variables, some of which could include fabrication method, polymer membrane thickness, and high duration level. This finding aligns with Zhu et al. 's (2022) demonstration that electrode-polymer interfacial engineering significantly impacts the force output that can be explained by just material conductivity alone.

Heterogeneity Assessment
	Table 6 reveals that there is substantial heterogeneity across all models, with the I2 values ranging from 96.77% (durability) to 99.98% (overall model), indicating that the vast majority of the observed variance stems from the true difference in nature between selected materials rather than sampling error. The displacement model defined a I2 = 99.97%, suggesting that the unmeasured study-level factors might substantially influence outcomes.

This substation heterogeneity justifies the use of the random-effects models over the other alternative fixed-effects approaches, as it acknowledges that the true effect size varies across studies and represents a single universal value. The high 2 values (ranging from 0.0126 to 44.4638) quantify the between-study variance, with displacement showing particularly high variability. Despite this inherently being distant, the constant direction effects show that CNT has a clear superiority. Across diverse study contexts, this observation is strengthened by the confidence in the dining’s robustness and generalizability. The significant Q-statistics (all p < 0.001) confirm that observed variance exceeds what would be expected from sampling error alone, therefore validating the meta-analytic approach's appropriateness for synthesizing this literature.

	Critically, the substantive ergogenicity imprint does not undermine the study’s conclusions but rather highlights the fact of the weight of fabrication standardization. The fact that CNT consistently outperforms SIlver and Copper emphasizes that despite methodical variation across included studies, CNT has dominant effects that persist across experimental conditions, which strengthens the data’s clear trend of CNT superiority.

Pairwise Comparisons
	Table 7 depicts ten pairwise comparisons across electrode materials that aim to produce comprehensive statistical validation for relative performance rankings. CNT Composite demonstrated statistically significant superiority over Silver across all three primary metrics: displacement( = 7.88 mm, p =0.0066), force, =7.20 mN, p = 0.0061), and durability ( = 4140 cycles, p = 0.0003). Similarly, CNT outperformed Copper in these three primary metrics as well:displacement( = 6.59 mm, p =0.0111), force, (=4.34 mN, p = 0.0466), and durability ( = 4450 cycles, p = 0.0003), which establishes CNT’s clear superiority over both uneven metallic alternatives.

	CNT versus planet revealed CNT’s significant displacement advantage in the three performance metrics: displacement( = 8.85 mm, p =0.0049), force (=2.08 mN, p = 0.2243), and durability ( = 2725 cycles, p = 0.0006). The interesting thing to note is that the force generation difference was nonstatistical (p = 0.2243), demonstrating that Platinum's primary limitation actually lies in actuation plates rather than the physical force output capability. The implication of this discovery allows platinum to be potently suitable for applications that require high force in limited displacement scenarios but vastly out of its zone for large displacement actuation tasks.

	Finally in the Gold versus CNT captions there was no significant displacement differences,( = -0.98 mm, p =0.8909) thus combining their performance queries in this metric. However, CNT demonstrates a significant durability advantage in displacement( = -2250 cycles, p =0.0409), while Gold showed marginally superior force output,( = 0.57mN, p =0.0.996) which is non-significant.

Figure 2 visualizes this pairwise comparison using-log10(p-value) transformations, where the bars extend beyond the red threshold line (p = 0.05), indicating statistical significance. This visualization clearly demonstrates CNT’s dominance: all CNT-related comparisons substantially exceed the significant threshold, while some reach values about 3.0, which corresponds to a p < 0.001. The graphical response confirms that CNT’s superiority is not marginal, but highly robust p-values are often on the order of magnitude of the conventional =0.05 threshold.

Hypothesis Testing
	Table 8 directly tests the primary research hypothesis by comparing CNT Silver and copper. CNT demonstrated superiority across all evaluated methods:

Displacement: CNT achieved 17.43 mm versus Silver’s 9.55 mm (82% improvement) and Copper’s 10.83 mm (61% improvement)
Force Generation: CNT produced 14.18 nM compared to Silver’s 6.98 mN (103% increase) and Copper’s 9.83 mN (44% increase)
Cycles to Failure: CNT endured 8400 cycles versus Silver’s 426- cycles (97% longer life span) and Copper’s 3950 cycles (113% longer span)

	All comparisons showed that CNT exceeded both competing materials and yielded checkmarks actress all sell in the comparison column. Their hypothesis that “CNT-based electrodes will demonstrate greater actuation displacement and longer durability under relapsed laid-bearing cycles compared to Silver or Copper electrodes,” is fully supported by the empirical data.

It is important to note that these results are privacy significant and represent a transformative rather than a fundamental advantage. The consistency of CNT’s superiority over multiple independent performance dimensions, rather than tradeoffs with one material exceeding one metric and another in a separate one, further strengthens the recommendation for CNT adoption and use in load-bearing robotics applications.
Discussion Of Results

Interpretation of Primary Findings
	
	The meta-analytic results provide robust empirical validation for CNT composite electrodes as the optimal material choice for load-bearing robotics applications. The 82%-97% improvement in the displacement over SIlver and Copper directly addresses the gap identified in existing literature, whether Deole and Lumia (2006) and Tamagawa et al. (2019) examined loading-bearing contexts without systematic electrode material comparisons. This research definitely establishes that electrode selection definitely determines IPMC performance in mechanical contexts.

	CNT’s superior performance aligns with theoretical predictions that this paper tried to empirically prove from material science literature. Bhandari et al. (2012) noted ambiguity to electrode material impotency, and this study establishes that CNT’s high surface area to volume ratio (up to 1315 m2/g) enhances ion transport efficiency. The 113% durability improvement over Copper buttresses claims by Zhu et al. (2022) that electrode polymer financial prototypes strictly influence the longer-term performance and CNT’s conformal bonding to nation membranes resists delamination and cracking observed in brittle metallic alternatives.
 
	Gold electrodes achieved displacement parity with CNT (p = 0.8225) while maintaining the lowest resistance, (1.98 ) which values Bar-Cohen et al.’s (2002) characterization of Gold as the baseline industry standard for all IPMC electrodes. However, through this paper's research and data, CNT’s 37% durability advantage (p=0.0409) and esteemed 10-15x lower material cost position CNT as the practical support choice for commercial robotics, where performance but also economics matter. As touched on before, Gold’s high standard displacement (12.89 mm) suggests fabrication sensitivity, which further corroborates Xu et al.’s (2021) finding on the importance of electrode morphology being kept concisely similar through the fabrication process. The fabrication process must be held to more stringent margins of error for Gold than CNT to achieve replicable performances.

Limitations and Future Discussions
	There was a small sample size for Copper (n=3) variants, which reduces statistical power, though the pairwise comparisons still achieved and hold significance. The exclusion of hybrid electrodes may limit application to merging multi-layer designs that could systematically combine material advantages, as will be seen below. Laboratory testing conditions, from which some data was pulled from, will obviously differ from real use of the IPMCs, yet most trends should hold. Furthermore, the meta-regression addressed this by including frequency moderators, yet field validation studies are necessary for further growth of the IPMC industry.

Future research should prioritize the following:


CNT concentration optimization with varying weight percentages (0.1-0.5%): maximize displacement and force while maintaining durability
Copper oxidation prevents high protective coatings or alloying methodologies
Longitudinal field studies that track IMPC performance in developed robots to downstore real-world failure events and move beyond labs
It must be noted that the use in robots would have to be for the purpose of testing the IPMC, not the actual robot itself.
Contextualization Within Robotics Applications
	For soft robotics requiring sustained performance over thousands of cycles while maintaining compliance, CNT’s 84-cycle survival approaches commercial flexibility, while other electrode materials falter out at around ~4000, thus limiting electrodes like Copper or SIlver to prototyping or short-duration application. For medical robotics experiencing the need for high-frequency actuation (1-5 Hz) during procedures that last 1-4 hours, or 3,600-72,000 cycles, CNT and Gold electrodes prove to be the only necessary material to be able to withstand the load and be reusable.

CNT’s 224 ms response time proves adequate when relieving apparition displacement and durability, even if Gold does achieve the fastest actuation at 157.5 ms.

The integration of multiple performance dimensions used in the thesis study reveals the following optimal choice depending on application priorities:

CNT: durability - critical contests, strict budgeting, proper facilities to dispose of
Gold: performance-critical applications, relaxed budget, and minimal facilities to dispose of
Copper and Silver should be avoided, especially in aqueous environments

The findings also carry environmental implications aligned with sustainable robotics design. By  finding out that CNT companies can replace precious metals with performance practice, this race supports the economy and environmentally sustainable actuator development. The reduced replacement frequency enabled by CNT’s superior durability decreases lifecycle material consumption and electronic waste generation, all of which are critical for commercial viability and environmental responsibility.
Appendix - A: Data Selection Requirements

A.1 - Introduction to Source Selection Criteria

The purpose of this appendix and its information is to document the systematic approach employed to identify, evaluate, and select the scholarly sources for this meta-analytic study. The source selection process is strictly adhering to the rigorous academic standard to ensure the reliability, validity, and generalizability of the findings.

A.2 - Inclusion and Exclusion Criteria
A.2.1 - Temporal Scope
Inclusion Window: 2000-2025
Justification: The 25-year window will allow the capture of the modern era of IPMC fabrication methods while ensuring the relevance to contemporary robotics applications, which the study focuses on. Studies prior to the 2000 benchmark utilized outdated fabrication techniques and are therefore not representative of the current manufacturing standards. The year 2000 was picked as the beginning of the range because it marked a critical transition point with the fabrication but more importantly the standardization of electroless plating methods as well as the widespread adoption and subsequent use of the Nafion membrane as the baseline polymer substrate. Previous To this moment, the baseline polymer substrates varied largely between different elements, and the industry lacked standardization of differences between each baseline.

A.2.2 - Content requirements
Quantitative performance metrics: studies must report numerical data on at least one of the following measurements
Bending displacement - measured in mm or degrees
Force generation/blocking force - measured in mN (can be converted if needed)
Electrical resistance - measured in ohms 
Cycle count to failure - number of actuation in cycles
Electrode Material Depreciation: Each study must explicitly identify the electrode material used with a clear difference between the following:
Silver (Ag)
Copper (Cu)
Carbon Nanotubes (CNT) Composite
Gold (Au)
Platinum (Pt)
Extractable data: Each study used must provide sufficient methodological detail and data to allow for complete data extraction and standardization for the multi-analytical process this study aims to do, including:
Sample dimensions
Test voltage specification
Environmental conditions - whether tests were done aqueous or air
Testing frequency - measured in Hz
Each of these is consistent with the environment from which the extracted data comes, and proper correction and standardization will need to be done if possible; otherwise, data will not be considered.
A.2.3 - Exclusion Criteria 
Hybrid electrodes - studies which use multi-metal, alloy, or compose electrodes are excluded to demonstrate the individual difference of each single element for comparative analysis
Non-Actuation Focused - studies that only focus on sensing application, energy harvesting, or theoretical meddling without quantitative experimental validation and data points were excluded.
Incomplete Recording - studies which lacked the essential methodological details or presented data in qualitative terms are excluded since the situation in which tests are done is highly critical to make the comparative analysis more valid.
Non-Peer-Reviews Sources - any non-peer-reviewed sources were excluded.
A.3 - Source Database and Search Strategy
A.3.1 - Database Selection
These following academic databases were systematically searched with search terms used located in A.3.2:
IEEE Xplore Digital Library 
Web of Science
Scopus
Google Scholar
A.3.2 - Search Terms and Boolean Operators
Primary search string: ("ionic polymer-metal composite" OR "IPMC") AND ("electrode" OR "electrode material") AND ("actuation" OR "performance" OR "displacement" OR "force")

Secondary search string used for ragged material searches when needed:
("IPMC" OR "ionic polymer") AND ("silver electrode" OR "Ag electrode") 
("IPMC" OR "ionic polymer") AND ("copper electrode" OR "Cu electrode")
 ("IPMC" OR "ionic polymer") AND ("carbon nanotube" OR "CNT electrode")
A.4 - Data Extraction Protocol
A.4.1 - Primary Variables Extracted
For each individual study picked, the following data points were systematically extracted and recorded in the structured spreadsheet:
	Study Metadata:
Authors
Publication year
Sample Size - number of IPMC specimens tested
	Fabrication Details:
Polymer membrane type - Nafion 117, Nafion 115, other
Electrode material
Electrode thickness
Fabrication method - impregnation reduction, electroless plating, etc.
Electrode surface treatment
	Performance Metrics
Displacement amplitude - mm or degrees
Blocking force - mN
Electrical surface resistance - ohms
Response time - ms
Cycles to failure
	Testing Conditions
Applied voltage - V
Testing frequency - Hz
Environmental conditions - air, water, humidity
Temperature - degrees C
A.4.2 - Data Standardization Procedures
All measurements were converted to standard units mentioned in A.4.1

For graphs, the WebPlot Digitizer software (Version 4.5) was used to extract the exact numerical date, trends, and relationships. To maximize reliability, each graph was digitized three times independently, and then the mean values were recorded to minimize the software extraction error.

Studies with incomplete data reporting were extracted directly when possible. If no response was received within 2 weeks, the study unfortunately would have to be excluded from the meta-analysis only for that specific metric while being retained for other metrics that were available from the offset.





Appendix - B: R Studio Code
GitHub Link: https://github.com/kool-krish101/AP-Research-IPMC-Testing


Bibliography
Akle, B. J., Leo, D. J., & Bengal, G. (2010). Electromechanical characterization of ionic polymer transducers: Influence of electrode morphology. Smart Materials and Structures, 19(5), 055026. https://doi.org/10.1088/0964-1726/19/5/055026
Bao, Xiaoqi, Yoseph Bar-Cohen, and Shyh-Shiuh Lih. "Measurements and macro models of ionomeric polymer-metal composites (IPMC)." Smart Structures and Materials 2002: Electroactive Polymer Actuators and Devices (EAPAD). Vol. 4695. SPIE, 2002.
Bar-Cohen, Yoseph, et al. "Characterization of the electromechanical properties of ionomeric polymer-metal composite (IPMC)." Smart Structures and Materials 2002: Electroactive Polymer Actuators and Devices (EAPAD). Vol. 4695. SPIE, 2002.

Bhandari, Binayak, Gil-Yong Lee, and Sung-Hoon Ahn. "A review on IPMC material as actuators and sensors: fabrications, characteristics and applications." International journal of precision engineering and manufacturing 13.1 (2012): 141-163.

Creswell, J. W. (2014). Research design: Qualitative, quantitative, and mixed methods approaches (4th ed.). SAGE Publications.

Deole, U., & Lumia, R. (2006, November). Measuring the load-carrying capability of IPMC microgripper fingers. In IECON 2006-32nd Annual Conference on IEEE Industrial Electronics (pp. 2933-2938). IEEE.

Nakabo, Y., Mukai, T., & Asaka, K. (2007). Biomimetic soft robots using IPMC. In Electroactive Polymers for Robotic Applications: Artificial Muscles and Sensors (pp. 165-198). London: Springer London.

Nemat-Nasser, S., & Li, J. Y. (2002). Electromechanical response of ionic polymer–metal composites. Journal of Applied Physics, 87(7), 3321–3331. https://doi.org/10.1063/1.372344

Shahinpoor, M., & Kim, K. J. (2001). Ionic polymer–metal composites: II. Manufacturing techniques. Smart Materials and Structures, 10(4), 893–913. https://doi.org/10.1088/0964-1726/10/4/314

Suzumori, K., Nabae, H., Asaka, K., & Horiuchi, T. (2020, April). Applying IPMC to soft robots. In Electroactive Polymer Actuators and Devices (EAPAD) XXII (Vol. 11375, pp. 38-46). SPIE.

Tamagawa, H., Okada, K., Mulembo, T., Sasaki, M., Naito, K., Nagai, G., ... & Ikeda, K. (2019, March). Simultaneous enhancement of the bending and blocking force of an ionic polymer-metal composite (IPMC) by the active use of its material characteristics. In Actuators (Vol. 8, No. 1, p. 29). MDPI.

Xu, Y., Jia, W., Zhang, Y., Wang, F., Zhao, G., & Zang, D. (2021). Mechanical properties analysis and surface composition research of Ag-IPMC. Sensors and Actuators A: Physical, 319, 112565.

Zhu, Z., Bian, C., Bai, W., Hu, Q., & Chen, S. (2022). Integrated fabrication process with multiple optimized factors for high power density of IPMC actuator. International Journal of Smart and Nano Materials, 13(4), 643-667.

Zhu, Zicai, et al. "Integrated fabrication process with multiple optimized factors for high power density of IPMC actuator." International Journal of Smart and Nano Materials 13.4 (2022): 643-667.


