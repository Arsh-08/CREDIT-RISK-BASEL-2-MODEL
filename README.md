# CREDIT-RISK-BASEL-2-MODEL
Overview
This project builds a fully dynamic Basel II Credit Risk Model in Excel for a 15-loan Indian loan portfolio. It computes Expected Loss (EL), Unexpected Loss (UL), Risk-Weighted Assets (RWA), and Regulatory Capital for each borrower — and stress-tests the entire portfolio across three macroeconomic scenarios.
Every number in the model is driven by live Excel formulas (264 total). Change any input in the Assumptions sheet and the entire model updates automatically.

Portfolio
15 real Indian borrowers across sectors:
BorrowerSectorRatingAsset ClassTata Steel LtdMetals & MiningBBBSenior Secured LoanReliance RetailConsumer/RetailASenior Unsecured LoanHDFC Home LoansMortgageAAResidential MortgageIndiGo AirlinesAviationBBSenior Secured LoanAdani PortsInfrastructureASenior Secured LoanYes Bank LtdBanking (NBFC)BSubordinated DebtGovt of India BondSovereignAAASovereignVedanta ResourcesMetals & MiningBSenior Unsecured LoanGodrej PropertiesReal EstateBBBResidential MortgageZomato LtdTechnologyBBSenior Unsecured LoanKotak Mahindra BankBankingAASenior Secured LoanONGC LtdEnergy/PSUAAASovereign+ 3 Retail BorrowersRetailBBB–BBPersonal Loan / Credit Card
Total Portfolio Value: ₹1,00,00,000+ (₹1 Crore+)

Key Results
MetricValueTotal EAD₹14,385 LakhsTotal Expected Loss (Normal)Calculated dynamicallyTotal RWACalculated dynamicallyRegulatory Capital Required (8% CAR)Calculated dynamicallyRecession EL (PD ×2.5x)~2.5× Normal ELSevere Stress EL (PD ×5x)~5× Normal EL
All values update when you change inputs in the Assumptions sheet.

Methodology
Core Basel II Formula
Expected Loss (EL) = PD × LGD × EAD

Unexpected Loss (UL) = EAD × LGD × √(PD × (1 − PD))

Risk-Weighted Assets (RWA) = EAD × Risk Weight

Regulatory Capital = RWA × 8%   (Basel II Pillar 1 Minimum CAR)
Basel II Risk Weights Applied
Asset ClassRisk WeightSovereign (India)0%Residential Mortgage35%Retail (Personal/Credit Card)75%Corporate (all other)100%
Scenario Stress Multipliers
ScenarioPD MultiplierLGD MultiplierNormal (Base)1.0×1.0×Recession2.5×1.2×Severe Stress5.0×1.4×

Model Structure — 5 Sheets
Sheet 1 — Dashboard
Project overview, navigation guide, key concept definitions (EL, UL, PD, LGD, EAD, RWA, CAR), and colour-coding legend.
Sheet 2 — Assumptions ← Start Here
All inputs in one place:

PD by credit rating (AAA → D, based on Basel II IRB guidelines)
LGD and Risk Weights by asset class
Scenario stress multipliers (Normal / Recession / Severe)
Capital Adequacy Ratio parameters (8% minimum, 2.5% conservation buffer)

Blue cells = inputs you can change. Everything else is a formula.
Sheet 3 — Loan Book
Individual loan calculations for all 15 borrowers:

EL, UL, RWA, Regulatory Capital per loan
EL as % of EAD
Portfolio totals row

Sheet 4 — Scenario Analysis
Stress test results for all 3 scenarios side by side:

EL under Normal, Recession, Severe Stress
Portfolio-level summary comparison
Traffic light status (✓ Base / ⚠ Elevated / ✗ Severe)

Sheet 5 — Summary

8 portfolio KPIs (EAD, EL, UL, RWA, Capital, EL Rate, Capital Ratio, Loan Count)
Scenario comparison table
Basel II regulatory interpretation (EL → provisions, UL → capital, RWA → CAR)


How to Use
1. Download Credit_Risk_Basel_II_Model.xlsx
2. Open in Microsoft Excel or Google Sheets
3. Go to the Assumptions sheet
4. Change any blue cell (PD, LGD, EAD, stress multipliers)
5. All sheets update automatically

Regulatory Context
This model is built around Basel II Standardised Approach:

Pillar 1: Minimum capital requirement = RWA × 8%
Pillar 2: Supervisory review (stress testing scenarios simulate this)
Pillar 3: Market discipline (summary sheet mirrors disclosure format)

Under Basel III, the Expected Shortfall (ES) replaces VaR for market risk, and the conservation buffer adds 2.5% to the minimum CAR (total 10.5%). The model includes this parameter in the Assumptions sheet.

Skills Demonstrated
Credit Risk Modelling · Basel II Standardised Approach · PD/LGD/EAD Framework · Stress Testing · Scenario Analysis · Regulatory Capital Calculation · Excel Financial Modelling · Portfolio Risk Management · FRM Part II — Credit Risk

Limitations & Extensions
The model uses Standardised Approach risk weights — blunt instruments that assign the same 100% weight to AAA and BB corporates alike. A natural extension would be the Internal Ratings-Based (IRB) Approach, which uses bank-estimated PDs to compute risk weights more precisely. This is exactly why Basel moved to IRB for sophisticated banks.
