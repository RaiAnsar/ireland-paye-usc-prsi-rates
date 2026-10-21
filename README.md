# Ireland PAYE, USC and PRSI rates for 2026 and 2027 (Budget 2027)

The parameters an Irish take-home pay calculation needs, in one JSON file: income tax rates and standard-rate bands, the personal, employee and home carer credits, USC bands and the exemption threshold, and Class A employee PRSI with its mid-year rate change. 2026 is the tax year in force; 2027 carries the Budget 2027 changes announced on 6 October 2026.

## Files

- `rates.json`: the 2026 and 2027 parameters. Money is in euro, rates are decimals, and `"up_to": null` marks the top USC band.
- `take-home-examples.csv`: yearly take-home pay for ten single and married cases in both years, for testing your own calculation against.

## What changes in 2027

| Item | 2026 | 2027 |
|---|---|---|
| Standard-rate band, single | €44,000 | €46,500 |
| Standard-rate band, married, one income | €53,000 | €55,500 |
| Married, two incomes | €53,000 plus the lower income up to €35,000 | €55,500 plus the lower income up to €37,500 |
| Personal tax credit, single | €2,000 | €2,125 |
| Employee tax credit | €2,000 | €2,125 |
| Home Carer Tax Credit | €1,950 | €2,050 |
| USC 2% band ends at | €28,700 | €30,300 |
| Employee PRSI, Class A | 4.2% to 30 September, 4.35% from 1 October | 4.35% to 30 September, 4.5% from 1 October |

Tax rates (20% and 40%) and the other USC bands (0.5% to €12,012, 3% to €70,044, 8% above) do not change.

## Worked check: single, €45,000, 2026

- Income tax: €44,000 at 20% plus €1,000 at 40% is €9,200, less €4,000 of credits: €5,200.
- USC: 0.5% of €12,012 plus 2% of €16,688 plus 3% of €16,300: €882.82.
- PRSI: 4.2% of weekly pay to 30 September and 4.35% after, over 52 weeks: €1,906.97.
- Take-home: €37,010.21. Under the 2027 parameters the same salary takes home €37,409.00.

Three details that catch out simple calculators:

- USC is all or nothing at €13,000: at or below it you pay none, above it USC applies to all of your income.
- PRSI is charged per week on the whole week's pay once it passes €352, with a PRSI credit between €352.01 and €424 a week, so monthly or fortnightly payroll can differ by a few euro from a 52-week estimate.
- For a married couple with two incomes, the band rises above €53,000 by the lower earner's income, up to €35,000 in 2026 (€37,500 in 2027).

## Sources

Checked on 15 October 2026:

- Revenue, tax relief charts: https://www.revenue.ie/en/personal-tax-credits-reliefs-and-exemptions/tax-relief-charts/index.aspx
- Revenue, USC standard rates and thresholds: https://www.revenue.ie/en/jobs-and-pensions/usc/standard-rates-thresholds.aspx
- Revenue, employee tax credit: https://www.revenue.ie/en/personal-tax-credits-reliefs-and-exemptions/income-and-employment/employee-tax-credit/index.aspx
- Department of Social Protection, PRSI contribution rates and user guide (SW 14, January 2026): https://assets.gov.ie/static/documents/cb168977/PRSI_C20260116_Contribution_Rates_and_User_Guide_-_SW_14_-_English_Version_-_January_2026_.pdf-web.pdf
- Budget 2027 tax policy changes: https://assets.gov.ie/static/documents/c6792805/Budget_2027_Tax_Policy_Changes_v2.pdf

The figures come from [irishtakehome.com](https://irishtakehome.com/), a take-home pay calculator for Ireland that shows every step for your own salary, single or married, in 2026 or 2027. This file is reference data, not tax advice.

## Licence

CC BY 4.0. Credit irishtakehome.com.
