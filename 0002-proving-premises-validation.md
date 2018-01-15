# 2. Proving Premises Validation

Date: 2018-01-15

## Status

Proposed

## Context

FBOs currently register food businesses at an address, and this information is then submitted to a Local Authority. This address data is not currently validated against a register of addresses nor organisations. This then adds the potential to register a business against a non-existent address, accidentally register a business to the wrong address, which can then waste time on the LA's part visiting the wrong address. Therefore as part of the registration process we would like to verify the submitted businesses name and address to verify its presence.

In order to do the above, we evaluated several address data services to assess their suitability for our use case.

## Decision

Land Registry - The data from LR is not suitable for our use case. This service holds data on prices paid, transactions and UK House Price Index. There is also separately dataset available with information on Commercial and Corporate Ownership.

Ordnance Survey - Places API allows you to search by postcode, where you can then verify the organisation name and address against a set of results.

Companies House - It is possible to use their APIs to search for a businesses registered address given you supply a company number.

Google APIs - It is possible to use the Places API to search for an organisation at an address.

## Consequences

