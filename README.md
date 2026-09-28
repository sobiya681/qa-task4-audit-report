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

## Findings Table

| # | View | Screen Size | Page / Element | Issue Description | Severity | Screenshot |
| 1 | Desktop | 1920×1080 | Header search icon | Search icon too small to click easily | Low | `desktop_header.png` |
| 2 | Desktop | 1920×1080 | Search Box page | Page renders in narrow mobile column; majority of screen appears empty | High | `desktop_searchbox_broken.png` |
| 3 | Desktop | 1920×1080 | My Account page | Account page shows the same narrow mobile layout | High | `desktop_account_broken.png` |
| 4 | Tablet | 768×1024 | My Account page | Tablet layout doesn't work — page stays narrow like mobile | High | `tablet_account_broken.png` |
| 5 | Tablet | 768×1024 | Search Box page | Same narrow column issue | High | `tablet_searchbox_broken.png` |
| 6 | Tablet | 768×1024 | Homepage | Narrow column; sidebar takes too much width; only 3 products per row | Medium | `tablet_homepage_broken.png` |
| 7 | Tablet | 768×1024 | Icon row below search | Daraz Mart and Buy More cut off; no visible scroll indicator | Medium | `tablet_icons_cutoff.png` |
| 8 | Mobile | 390×844 | Icon row below search | Buy More icon partially cut off at right edge | Low | `mobile_icons_cutoff.png` |
| 9 | Mobile | 390×844 | Navbar | Navbar content spills past the right edge and overflows | Medium | `mobile_navbar_overflow.png` |
| 10 | Mobile | 390×844 | Floating action buttons | Floating icons stack on top of each other and cover the footer | Medium | `mobile_floating_overlap.png` |

## Key Issues Found

1. **Responsive layout failure on tablet and desktop** : Search Box, My Account, and Homepage render in narrow mobile columns at 768px and 1920px widths
2. **Header navbar overflow** : category items cut off on mobile without visible scroll indicator
3. **Icon row cut off** : Daraz Mart and Buy More icons cut off on tablet and mobile
4. **Floating action buttons overlap** : icons stack on top of each other, covering footer content

## AI Usage

Used AI to identify edge cases such as slow-3G throttling and additional responsive breakpoints to test.

## Author

Sobiya  
QA Internship : Barakah Tech Labs
