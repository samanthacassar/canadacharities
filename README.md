# canadacharities

An analysis looking at 2018 charity information collected by CRA and requested & retrieved by Matthew Dubins in Jan 2020. The following provides an overview of the data in relation to the CRA data collection files and the format the data was received in.

A charity return with the CRA requires the completion of multiple forms. The main form is the [T3010 Registered Charity Information Return](https://www.canada.ca/content/dam/cra-arc/formspubs/pbg/t3010/t3010-fill-18e.pdf) form.

The data collected via this form is spread across several tables. The main financial data is captured in 2 tables (<b>Financial Section A_ B and C</b> and <b>Financial Section D & Schedule 6</b>), while each proceeding schedule has its own table:
<b>
- Schedule 1_ Foundations
- Schedule 2_ Activities Outside Canada
- Schedule 3_ Compensation
- Schedule 5_ Non-Cash gifts
- Schedule 7_ Description
- Schedule 7_ Political Activities - Outside Canada
- Schedule 7_ Political Activities - Resources
</b>

Finally, the text information capturing new and ongoing programs in this same form is captured in separate table <b>New and Ongoing Programs</b>.

Other tables:

- The <b>Gift</b> table characterizes money transfers to donation recipients and other organizations, captured in an additional form ([T1236 Qualified Donees Worksheet/Amounts provided to other organizations](https://www.canada.ca/content/dam/cra-arc/formspubs/pbg/t1236/t1236-fill-18e.pdf)).
- The <b>Ident</b> table looks to include profile data for each CRA account.
- The <b>Trustee</b> table includes data captured in a separate form, [T1235 Directors/Trustees and Like Officials](https://www.canada.ca/content/dam/cra-arc/formspubs/pbg/t1235/t1235-fill-18e.pdf).

Files with a hashtag in front of the name serve as lookup tables.

Glancing at the csv files in Excel, here is what we know about these files:

## REGISTERED
<b> Financial Section A_B and C</b>

- Data reflects fiscal years that ended in 2018. These dates differ across entries.
- Each row represents a registered entity and each column represents a different part of the T3010 Registered Charity Information Return Form.
- Each row has a BN/Registration number, which links to the <b>Ident</b> table. (to confirm)
- Columns 1200-1220 look to refer to different areas of programming that the charity engages in (using codes from <b># Programs</b> lookup table), along with what proportion of their resources/efforts are allocated to this category. It is unclear where this data is captured, however, as these fields are not present in the form.
- Columns 1510-5830 appear to capture different fields within the form. Most are sparsely filled.

## REVOKED/ANNULLED
The tables in the second directory look to characterize which CRA charity accounts revoked or had their charity status annulled. A <b># Reason</b> lookup table provides different reason codes for doing so.

The <b>List of registered charities</b> table here looks identical with the <b>Ident</b> table in the Registered directory.