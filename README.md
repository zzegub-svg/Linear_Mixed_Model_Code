# Linear_Mixed_Model_Code

Mechanical Work Analysis – Split-Belt Treadmill
Overview

This R Markdown script analyzes lower-limb joint mechanical work during split-belt treadmill walking across four experimental periods:

Late Baseline

Early Adaptation

Late Adaptation

Post Adaptation

The script assigns periods based on subject-specific transition steps, averages joint mechanical work within each period, runs linear mixed models, performs Holm-adjusted post hoc comparisons, and generates mean ± SEM plots.

Analysis Approach

Data reshaped to long format (Subject × Period × Variable)

Mechanical work averaged within each period

Linear mixed model for each joint variable:

Work ~ Period + (1 | Subject)

Post hoc pairwise comparisons using Holm correction

R Packages Used

tidyverse

lme4

lmerTest

emmeans

Required Input File

combined_subject_data_clean.csv

The dataset must contain:

File identifiers with subject labels

Step numbers

Joint work variables (ankle, knee, and hip; positive and negative work)

Update the file path in the script before running.

Output

Linear mixed model summaries for each joint work variable

Holm-adjusted post hoc comparisons

Line plot of joint work across periods (Mean ± SEM)

Knitted HTML report
