# AllergyIntolerance
The AllergyIntolerance is an optional resource that may be returned within the Patient/$everything Bundle. Its use within Ocean is limited to referral form prepopulation and the possibility of clinical decision support using the corresponding Ocean keyword @ptCpp.allg.

Since the full textual representation of this resource is the main requirement for Ocean's use cases, the resource's **text.div** narrative value is converted to plain text and used as the primary value.