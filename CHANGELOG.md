# Changelog

All notable changes to XRechnung Test Suite will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).
<!--
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).
-->

## NEXT

### Added
* Testcase 01.18: "Standard invoice with 1 line, 1 tax category AE, 1 payment means code 58@


## 2020-12-31

This release is compatible with XRechnung 2.0.1.

### Added

* `src/doc/test-overview.md` for further documentation of test cases
* Added construction invoice (04.03a-INVOICE_ubl.xml)

### Changed

* Corrected sums (04.01a-INVOICE_ubl.xml)
* Added BT-129, BG-29 und BG-30 to Sub Invoice Lines (04.01a-INVOICE_ubl.xml)
* Added newlines in BT-20 (01.10a-INVOICE_ubl.xml, 01.10a-INVOICE_uncefact.xml)
* Added BT-29 and BT-90 (03.01a-INVOICE_ubl.xml, 03.01a-INVOICE_uncefact.xml)
* Deleted BT-6 where BT-5 is equal (01.01a-INVOICE_*.xml - 01.15a-INVOICE_*.xml, 03.01a-INVOICE_*.xml, 03.02a-INVOICE_*.xml)

## 2020-07-31

This release is compatible with XRechnung 2.0.0.

### Added

* `docs/development.md` for further hints on developing test cases
* Pure technical test cases

### Changed

* All instances changed to specification id for XRechnung 2.0.0
* Restructured directory layout to differentiate business test cases for the standard only (CIUS) and with extension
* Validator configuration is now local only dependency for development
* Fix bug with invalid IBANs in some instances
* Adjustments to new CEN rules


### Removed

* Any dependency on XML Validator

## 2019-12-30

This release is compatible to XRechnung 1.2.2.

### Added

For UBL and UNCEFACT:

* 02.01a-INVOICE
* 02.02a-INVOICE
* 03.01a-INVOICE (energy bill test case from energy sector, and debited account)
* 03.02a-INVOICE (test case for credit card payments)

### Changed

* All test instances:
  * removed `schemaLocation` attribute
  * only valid IBANs for `BT-84 Payment account identifier`
  * renewed codes for `BT-81 Payment means type code`
* 01.13a-Invoice_uncefact.xml, 01.13-Invoice_ubl.xml:
  * Added data to `BT-31 Seller VAT identifier`
* 01.14a-Invoice_uncefact.xml, 01.14-Invoice_ubl.xml:
  * Corrected data on `BT-30 Seller legal registration identifier` and `BT-47 Buyer legal registration identifier`
* 01.15a-Invoice_ubl.xml:
  * Removed `cbc:DocumentTypeCode = 130` for `BG-24 ADDITIONAL SUPPORTING DOCUMENTS`

## 2019-06-30

This release is compatible to XRechnung 1.2.1.

### Changed

* For all UBL-instances changed to tests to `<cbc:Note>#ADU#Ordered in our booth at the convention</cbc:Note>`
 in case of presence of BT-21.
* Test case 01.14 changed to according to the separation of Invoice note (BT-22) and Invoice note subject code (BT-21).
* All test instances are now valid to XRechnung Version 1.2.1
* Changed constant value to `130` for BT-18 for all UBL instances. Test case 01.15 changes accordingly.

## 2018-12-14

This release is compatible to XRechnung 1.2.0.

### Added

* Changelog
* Distribution zip including all necessary content

### Changed

* All test instances are now valid to XRechnung Version 1.2.0
