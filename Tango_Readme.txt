ALTER TABLE ValidIBAN NOCHECK CONSTRAINT FK_ValidIBAN_Countries
UPDATE t 
 SET t.CountryID = s.Corrected
from #TempNewCountryID s,Countries t
where 
s.Existing = t.CountryID