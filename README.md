# Task 4: UI/UX & Responsive Design Audit

## Objective
Audit a web page's responsiveness across Desktop, Tablet, and Mobile views using Chrome DevTools. Document elements that break, overlap, or become unclickable.

## Application Under Test
Daraz.pk : https://www.daraz.pk

## Tools Used
- Google Chrome DevTools (Device Toolbar + Network Throttling)
- Google Sheets (Audit Matrix)
- Windows Snipping Tool (screenshots)
- GitHub

## Testing Approach

### Devices Emulated
| View   | Device Emulated | Screen Size |
| Desktop | Responsive      | 1920×1080   |
| Tablet  | iPad Mini       | 768×1024    |
| Mobile  | iPhone 12 Pro   | 390×844     |

### Pages Tested
- Homepage (`daraz.pk`)
- Search Box page (`daraz.pk/searchbox/`)
- My Account page (`member.daraz.pk/user/account`)
- Header navbar and footer regions

### Network Throttling
- Simulated Slow 3G connection to observe loading behavior and layout shifts under poor connectivity.

## Findings Summary

| Severity | Count |
| High     | 4     |
| Medium   | 4     |
| Low      | 2     |
| **Total**| **10**|

## Findings Table & Audit Files

- 📊 [Responsive_Audit_Report.xlsx](Responsive_Audit_Report.xlsx) — Full audit matrix with all 14 findings
- 📁 [screenshots/](screenshots/) — All evidence screenshots

## Key Issues Found

1. **Responsive layout failure on tablet and desktop** : Search Box, My Account, and Homepage render in narrow mobile columns at 768px and 1920px widths
2. **Header navbar overflow** : category items cut off on mobile without visible scroll indicator
3. **Icon row cut off** : Daraz Mart and Buy More icons cut off on tablet and mobile
4. **Floating action buttons overlap** : icons stack on top of each other, covering footer content

## AI Usage

Used AI to identify edge cases such as slow-3G throttling and additional responsive breakpoints to test.

## Author

Sobia  
QA Internship : Barakah Tech Labs
