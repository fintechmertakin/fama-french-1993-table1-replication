# fama-french-1993-table1-replication
Replicates Table 1 from Fama &amp; French (1993) using CRSP stock data and the original factor construction methodology. Includes variable definitions, portfolio-formation rules, and replication of descriptive statistics for market, SMB, and HML factors for U.S. equities.
This project replicates Table 1 from Fama and French (1993), “Common Risk Factors in the Returns on Stocks and Bonds”, using Stata and U.S. stock data from CRSP. It demonstrates an empirical replication of the foundational Fama–French 3-Factor model and highlights the process of constructing the market, size, and value factors following the paper’s methodology.

Stage 1 – Documentation Review

Extracts relevant methodological details from the original paper:

Sample period: July 1963 – December 1991

Universe: All non-financial, non-micro stocks listed on NYSE, AMEX, and NASDAQ

Variables: Market equity (ME), book-to-market equity (BE/ME), and returns (RET)

Portfolio formation:

Size breakpoints based on NYSE median market equity

Book-to-market breakpoints using NYSE 30th/70th percentiles

6 portfolios formed from the intersections (Small/Big × Low/Medium/High BE/ME)

Factor construction:

SMB = average return of small portfolios − average return of big portfolios

HML = average return of high BE/ME − average return of low BE/ME

MKT = value-weighted return on all stocks − risk-free rate

Stage 2 – Replication of Table 1

Uses monthly CRSP data for U.S. stocks, filters for ordinary shares (share codes 10 & 11), and merges with Compustat book-equity data via the CRSP–Compustat link (CCM).

Calculates market equity, book-to-market ratio, and portfolio assignments following Fama–French rules.

Computes monthly portfolio returns and aggregates to produce mean, standard deviation, and correlation statistics matching Table 1.
