SEPA Direct Debit (SDD) XML Generator
====================================

### How to use?

See *index.php* for an example how to create a SEPA message.
  * Set the namespace according to your requirements. By default, the EPC message scheme `urn:iso:std:iso:20022:tech:xsd:pain.008.001.02` is set.<br>
  * Note that the `SEPAGroupHeader` must exist only once per message.
  * Per message you can include multiple `SEPAPaymentInfo` blocks (e.g. one per debit sequence type).
  * Per `SEPAPaymentInfo` block multiple transactions `SEPADirectDebitTransaction` may be added.
  * It is possible to validate a message against an XSD scheme prior to generating an XML file. Therefore, have a look at the 
  commented statement near the end of *index.php*. Currently, we include out-of-the-box support for the following schemes:
    * EPC: `pain.008.001.02`
    * Austria: 
        * `pain.008.001.02.austrian.004.Korrigendum`
        * `pain.008.001.02.austrian.003`
    * Germany:
        * `pain.008.001.02_GBIC_3` (valid from 17.11.2019)
        * `pain.008.001.02_GBIC_2` (valid from 18.11.2018)
        * `pain.008.001.02_GBIC_1` (valid from 20.11.2016)
        * `pain.008.003.02`

### What is this?

The Single Euro Payments Area (SEPA) is a payment-integration initiative of the European Union for simplification of bank transfers denominated in euro.
Based on your input data, this script facilitates the process of generating a SEPA-compliant XML file for direct debit.

---

#### LICENSE

![CC BY-NC](http://i.creativecommons.org/l/by-nc/3.0/88x31.png)

This work is licensed under the Creative Commons Attribution-NonCommercial 3.0 License. To view a copy of this license, visit http://creativecommons.org/licenses/by-nc/3.0/.
For commercial use please contact sales@web-wack.at