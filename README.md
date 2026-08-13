# Manufacturing Analytics Dashboard

Quality and rejection analysis on garment labeling production data, covering November 1 to November 27, 2015. The dataset spans over 86.72 million units across the factory's core product lines. Built with SQL, Excel, Power BI, and Tableau.

## Business Problem

The factory needed to find where production was leaking money: which departments, machines, and shifts were driving rejections, and how much material was going to waste between what was scheduled (Work Order quantity) and what actually shipped clean.

## KPIs Tracked

- Total Manufactured Quantity: units pushed into production
- Total Processed Quantity: units that completed their operational stage (cutting, folding, etc.)
- Total Rejected Quantity: units flagged defective or out-of-spec during quality checks
- Overall Rejection Rate (%): the core quality health metric
- Wastage Gap: the difference between scheduled WO quantity and actual completed output

## Dashboards

Three versions of the same analysis, built separately in Excel, Tableau, and Power BI to compare each tool's dashboarding approach on the same dataset. Screenshots are in `/dashboards`.

## Key Findings

The factory's overall rejection rate came out to 0.61%, comfortably under the 1% threshold most plants target. That number looks good on its own, but it hides a real split between departments.

Printed Labels ran at 0.01% rejection: only 3,221 rejections across 28.53 million units. Woven Labels ran at 0.90%: 521,508 rejections out of 58.18 million units. Almost all the factory's quality problems trace back to one line.

One operator, Shruti Singh, is tied to 520,867 of the 524,729 total rejections in the dataset. That's close to the entire rejection count sitting with a single employee profile, which points more toward a data entry, mislogging, or machine-assignment issue than a genuine performance problem.

On the equipment side, three machines account for most of the mechanical failures: C007 (33.6k rejections), C039 (26.4k), and C022 (23.4k).

## Recommendations

- Audit Shruti Singh's shift data directly, check for logging errors or a machine-assignment mixup before treating this as an operator performance issue
- Pull C007, C039, and C022 offline for calibration, with a focus on their cutting and weaving alignment modules
- Apply the Printed Labels department's QC and maintenance schedule to the Woven Labels line, since it's the one line already hitting near-zero rejections at comparable volume

## Conclusion

The factory's headline rejection rate is misleading on its own: it looks strong mainly because Printed Labels is dragging the average down. Woven Labels is where the real risk sits, and it's the line that needs the calibration work and the standardized QC process. Next step is refreshing the dashboard weekly to track whether the Woven Labels rate moves toward the 0.05% baseline Printed Labels already hits.

## Tools

SQL (MySQL), Power BI + DAX, Excel, Tableau

## Team

Group 3: Sujata Sidray Karoli, Atharv Rajesh Kinjawadekar, Ashish Kumar, Dhareppa Suresh Maranur, Sangamesh Rakshe, Nitin Kumar Namdeo, Reshma Bollineni
