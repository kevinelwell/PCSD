I created a PowerShell script that queries the wigle.net's API searching for well-known pacemaker manufacturers MAC addresses in the hopes it might be useful to Law Enforcement and the FBI.

Currently, the script is using the following coordinates:

| Coordinates | Description |
|--------------|---------------------|
| 20.712  | Lesser Latitude |
| 34.789  | Greater Latitude |
| -100.006 | Lesser Longitude |
| -118.935 | Greater Longitude |

-------------------------------------------------------------------------------------------------------------------------------------------------
GROK output:
There are primarily 4 to 5 major manufacturers of pacemakers actively supplying the US market as of 2026, based on market share data,
FDA approvals, and industry analyses. These companies dominate the vast majority of implants and sales (often cited as controlling ~90%+
of the market collectively).

The key players consistently identified across recent reports (e.g., GlobalData, iData Research, market analyses from 2023–2025) are:

Medtronic (US-based operations, headquartered in Ireland but major US presence; often the market leader in the US).

Abbott Laboratories (includes legacy St. Jude Medical products; strong in leadless and MRI-compatible devices).

Boston Scientific (US-based; focuses on advanced pacing technologies).

Biotronik (German-based, but significant US market share and FDA-approved devices).

MicroPort Scientific (Chinese-based, growing presence in the US with FDA approvals).


Medtronic (especially CRM/cardiac division for BlueSync/BLE pacemakers):
Primary OUI: 54:FA:89 (Medtronic CRM-specific; confirmed in MAC vendor databases and BLE scanner discussions for pacemakers).
Alternative/related: 70:B3:D5:B3:4 (MA-S block, sometimes listed under Medtronic).

Abbott Laboratories (includes legacy St. Jude Medical; BLE in devices like myMerlin-enabled pacemakers/ICDs):
No single cardiac-specific OUI is prominently listed for pacemakers, but company OUIs include 00:13:DD (Abbott Diagnostics/Point of Care)
and others like 1C:C0:E1:2 or 70:B3:D5:94:3 (MA-M/MA-S blocks under Abbott subsidiaries). BLE MACs in Abbott cardiac devices often fall under 
these or inherited St. Jude ranges; no unique cardiac prefix is publicly tied exclusively to pacemakers.

Boston Scientific:
Primarily uses RF telemetry (not BLE) in many pacemakers; BLE may appear in communicators/programmers/accessories. Company OUI: 00:0F:19 (general Boston Scientific). 
No dedicated BLE OUI for pacemakers is documented in public sources—MACs, if present, follow standard 48-bit format under company prefixes.

Biotronik:
Primarily uses proprietary wireless (e.g., 401-406 MHz Home Monitoring), not standard BLE in core devices. Company OUI: 00:0B:C4 (BIOTRONIK GmbH & Co.). 
Bluetooth in accessories (if any) would use this or related prefixes; no BLE-specific pacemaker OUI confirmed.
MicroPort Scientific (growing in US with BLE in models like Alizea/Borea series):
No publicly listed specific OUI prefix in IEEE databases or vendor lookups for MicroPort cardiac/BLE devices (may inherit from prior owners like LivaNova/Sorin, 
which also lack prominent listings
-------------------------------------------------------------------------------------------------------------------------------------------------


-------------------------------------------------------------------------------------------------------------------------------------------------
Gemini output:
Below are the known MAC address prefixes for the primary manufacturers of pacemakers and cardiac devices:
Major Pacemaker Manufacturer MAC Prefixes
Manufacturer Known MAC Prefix(es) Notes / Division
Medtronic - 54:FA:89 - Registered specifically to Medtronic CRM (Cardiac Rhythm Management).
Medtronic - 70:B3:D5:B3:4A - smaller block (MA-S) often used for specific BlueSync™ technology devices.
Abbott - (St. Jude) - 00:13:DD - Registered under Abbott Diagnostics.
Abbott - (St. Jude) - 1C:C0:E1:2 - Registered under Abbott Medical Optics/Medical divisions.
Boston Scientific - 00:07:CF - Common OUI for Boston Scientific cardiac rhythm systems like LATITUDE™.
Biotronik - 00:09:A7 - Registered to Biotronik SE & Co. KG.
MicroPort (Sorin) - 00:0C:8C - Used for CRM devices originally under the Sorin Group brand.
-------------------------------------------------------------------------------------------------------------------------------------------------
