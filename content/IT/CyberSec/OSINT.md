---
tags:
  - it/cybersecurity
---
https://voters.cec.gov.ge/
https://what3words.com/
[C.A.S.E](https://www.globalcase.org/en/courses/summer-school/)

[[UG Hacking|UG Hacking]]
[[Neural OS/03 Tactical_Memory/IT/CyberSec/Hacking|Hacking]]

[Counterintelligence](https://en.wikipedia.org/wiki/Counterintelligence)

[Intel vs counterIntel](https://www.youtube.com/watch?v=o9CaEMZQ03c)



[IntelTechniques-Open-Source-Intelligence-OSINT-Course.23.10](file:///D:%5CVideos%5CIntelTechniques-Open-Source-Intelligence-OSINT-Course.23.10)

[OSINT Fundamentals](file:///D:%5CVideos%5COSINT%20Fundamentals)




## Valuable information Characteristics
- Accurate - Wrong info = wrong decision
- Timely - Late info is useless
- Relevant - Does it ==solve current problem==? Else it's noise 
- Complete - Missing data = Wrong conclusion
- Concise - Manageable
- Accessible - Hard to find = not helpful
- Verifiable - Check the source/truth

Here’s a **prioritized OSINT data list** (based on usefulness in real investigations):
## Online
---

### 🥇 1. **Username / Alias**
- 🔍 Reused across platforms, helps link accounts.
- Often leads to email, social, forums, leaks.
---
### 🥈 2. **Email Address**
- 🎯 Can be searched in breaches (HaveIBeenPwned), forums, WHOIS, LinkedIn.
- Connects to logins, metadata, even password dumps.
---
### 🥉 3. **Phone Number**
- 📞 Used in reverse lookups, WhatsApp profile scraping, Telegram, social networks.
- Helps geolocate, verify identity, and link aliases.
---
### 4. **Social Media Profiles**
- 🧠 Provides habits, friends, interests, locations, photos, political views, etc.
- Good for behavioral profiling and timeline building.
---
### 5. **IP Address**
- 📍 Can indicate rough location or ISP.
- Valuable when extracted from email headers or leaks.
---
### 6. **Photos (Metadata + Visual Clues)**
- 🖼️ EXIF may have GPS; content shows objects, surroundings, signs, timestamps.
- Used in **geolocation challenges** (like Bellingcat style).
---
### 7. **Real Name**
- 🧾 Helpful for registry/database search (gov, public records), but can be common.
- Alone not that useful, better with aliases or emails.
---
### 8. **Workplace / School**
- 🏢 Leads to org structure, colleagues, physical locations, routines.
- Used in spear-phishing and profiling.
---
### 9. **Geolocation Info**
- 🌍 Found via images, check-ins, events, IPs, backgrounds.
- Used to confirm physical presence or movement.
---
### 10. **Leaked Passwords**
- 🔓 Used to test credentials, uncover reused logins, or access platforms.
---
## In real life
Focus on these **7 key OSINT-style cues** in real-life convos to extract max intel (ordered by value):

---
### 🥇 1. **Usernames / Handles**

> "My Twitter is @johnny_boy92"
- Most valuable — links to online presence instantly.
---
### 🥈 2. **Emails or Domains**
> "Email me at [mike@acme.dev](mailto:mike@acme.dev)"
- Great for social scraping, breach search, WHOIS.
---
### 🥉 3. **Phone Numbers**
> "Text me on WhatsApp"
- Opens up Telegram, TrueCaller, and reverse search options.
---
### 4. **Places / Check-ins**
> "Last summer I was in Bali"
- Good for timeline building, photo matching, behavior analysis.
---
### 5. **Employer / Role**
> "I work at Tesla on the security team"
- Can map their org chart, find coworkers, or target company info.
---
### 6. **Names of Friends / Family**
> "My brother Alex works in crypto"
- Cross-reference to expand the network and find connections.
---
### 7. **Hobbies / Subcultures**
> "I love gunpla and 90s anime"
- Helps you narrow down forum or Reddit presence, niche platforms.
---

✅ Bonus Tip: Ask **open-ended questions** and listen for slips like:
- Dates (for timeline building)
- Habits ("I always run at 6am")
- Tech use ("I use ProtonMail")
Want this as a cheat card or add non-verbal cues too?


## Profiling 

If you're profiling a dangerous person (OSINT-style), here's the **ideal structure** for your report — sorted by priority & relevance:

---

### 🧠 **1. Identity**
- **Full name / aliases / nicknames**
- **Date of birth / age**
- **Known photos / physical description**
---
### 📱 **2. Digital Footprint**
- **Usernames** (across platforms)
- **Emails**
- **Phone numbers**
- **Social media links**
- **Breached credentials** (from HaveIBeenPwned etc.)
---

### 📍 **3. Location & Movement**
- **Current location** (confirmed or suspected)
- **Previous addresses**
- **Check-ins / GPS data / tagged photos**
- **IP logs (if available)**
---

### 🏢 **4. Employment & Affiliations**
- **Workplace / role**
- **Groups or organizations** (political, extremist, religious)
- **Known associates / network**
---
### 💬 **5. Behavioral Patterns**
- **Online behavior** (posts, threats, propaganda)
- **Habits / routines**
- **Languages spoken / slang used**
- **Preferred platforms / tools (e.g., Telegram, TOR)**
[[Pattern Recognition]]
---
### 🔫 **6. Threat Indicators**
- **Weapons shown or discussed**
- **Violent rhetoric**
- **Criminal record (if public)**
- **Flags from previous investigations / intelligence**
---

### 📄 **7. Evidence & Sources**
- **Screenshots** (messages, posts, threats)
- **Archived links**
- **Metadata (e.g., EXIF)**
- **Cross-verified sources (OSINT rules!)**
---

