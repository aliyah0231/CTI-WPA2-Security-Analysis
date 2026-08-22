# 📚 References

Dokumen ini berisi referensi utama yang digunakan dalam proyek **Threat
Intelligence & Vulnerability Assessment on WPA2-Personal Networks: From
4-Way Handshake Capture to MitM Risk Mitigation**.

> **Catatan:** Referensi dipilih dari sumber resmi/primer seperti MITRE
> ATT&CK, NIST NVD, CERT/CC, dokumentasi Wireshark, dan Aircrack-ng.

------------------------------------------------------------------------

## 1. MITRE ATT&CK --- Network Sniffing (T1040)

**MITRE ATT&CK.** *Network Sniffing --- Technique T1040.*

Digunakan sebagai referensi untuk pemetaan aktivitas pengamatan dan
penangkapan traffic jaringan dalam analisis threat intelligence.

-   MITRE ATT&CK ID: `T1040`
-   Tactics: Credential Access, Discovery
-   Reference: https://attack.mitre.org/techniques/T1040/

------------------------------------------------------------------------

## 2. MITRE ATT&CK --- Brute Force (T1110)

**MITRE ATT&CK.** *Brute Force --- Technique T1110.*

Digunakan sebagai landasan pemetaan risiko pengujian password. MITRE
membagi T1110 menjadi beberapa sub-technique, termasuk Password Guessing
(`T1110.001`) dan Password Cracking (`T1110.002`).

-   MITRE ATT&CK ID: `T1110`
-   Tactic: Credential Access
-   Reference: https://attack.mitre.org/techniques/T1110/

### Password Guessing --- T1110.001

-   Reference: https://attack.mitre.org/techniques/T1110/001/

### Password Cracking --- T1110.002

-   Reference: https://attack.mitre.org/techniques/T1110/002/

> **Catatan pemetaan:** Template tugas menggunakan `T1110.001` untuk
> WPA2 Handshake Capture & Offline Cracking. Pada MITRE ATT&CK saat ini,
> `T1110.001` bernama **Password Guessing**, sedangkan `T1110.002`
> bernama **Password Cracking**. Repository mempertahankan pemetaan dari
> instruksi tugas pada bagian utama, sementara perbedaan terminologi ini
> dicatat agar dokumentasi tetap transparan.

------------------------------------------------------------------------

## 3. MITRE ATT&CK --- ARP Cache Poisoning (T1557.002)

**MITRE ATT&CK.** *Adversary-in-the-Middle: ARP Cache Poisoning ---
Sub-technique T1557.002.*

Referensi ini digunakan untuk analisis risiko ARP Spoofing /
Man-in-the-Middle pada jaringan lokal.

-   MITRE ATT&CK ID: `T1557.002`
-   Parent Technique: `T1557 — Adversary-in-the-Middle`
-   Tactics: Credential Access, Collection
-   Reference: https://attack.mitre.org/techniques/T1557/002/

------------------------------------------------------------------------

## 4. NIST National Vulnerability Database --- CVE-2017-13077

**National Institute of Standards and Technology (NIST), National
Vulnerability Database.** *CVE-2017-13077.*

CVE ini menjadi salah satu referensi utama dalam pembahasan **KRACK (Key
Reinstallation Attack)** pada WPA/WPA2. NVD menjelaskan bahwa WPA/WPA2
dapat mengizinkan instalasi ulang Pairwise Transient Key (PTK) Temporal
Key selama four-way handshake pada implementasi yang terdampak.

-   CVE ID: `CVE-2017-13077`
-   Reference: https://nvd.nist.gov/vuln/detail/CVE-2017-13077

------------------------------------------------------------------------

## 5. CERT/CC --- KRACK Vulnerability Note

**CERT Coordination Center (CERT/CC).** *VU#228519 --- Wi-Fi Protected
Access (WPA) handshake traffic can be manipulated to induce nonce and
session key reuse.*

Referensi ini digunakan untuk memperkuat penjelasan mengenai manipulasi
WPA/WPA2 handshake, penggunaan ulang nonce/session key, dan Key
Reinstallation Attack.

-   Vulnerability Note: `VU#228519`
-   Related CVEs: CVE-2017-13077 dan keluarga CVE KRACK lainnya
-   Reference: https://www.kb.cert.org/vuls/id/228519/

------------------------------------------------------------------------

## 6. KRACK Research

**Vanhoef, M., & Piessens, F.** *Key Reinstallation Attacks: Forcing
Nonce Reuse in WPA2.*

Penelitian ini merupakan referensi akademik utama mengenai KRACK dan
menjelaskan kelemahan pada proses key reinstallation dalam WPA2 4-Way
Handshake.

-   Research information: https://www.krackattacks.com/
-   Paper: https://papers.mathyvanhoef.com/ccs2017.pdf

------------------------------------------------------------------------

## 7. Wireshark Documentation

**Wireshark Foundation.** *Wireshark User's Guide.*

Digunakan sebagai referensi untuk proses packet capture, display filter,
serta analisis paket jaringan termasuk traffic EAPOL.

-   Reference: https://www.wireshark.org/docs/wsug_html_chunked/

------------------------------------------------------------------------

## 8. Aircrack-ng Documentation

**Aircrack-ng Project.** *Aircrack-ng Documentation.*

Digunakan sebagai referensi tools wireless yang digunakan pada
lingkungan laboratorium, termasuk komponen Aircrack-ng suite.

-   Reference: https://www.aircrack-ng.org/documentation.html

------------------------------------------------------------------------

## 9. IEEE 802.11 Wireless LAN

**IEEE Standards Association.** *IEEE 802.11 Wireless LAN Standards.*

Digunakan sebagai referensi umum untuk teknologi dan protokol jaringan
wireless IEEE 802.11 yang menjadi dasar jaringan Wi-Fi.

-   Reference: https://standards.ieee.org/standard/802_11-2024.html

------------------------------------------------------------------------

## 🔎 Mapping Referensi terhadap Analisis

  Bagian Analisis               Referensi Utama
  ----------------------------- ---------------------------------------
  Network Sniffing              MITRE ATT&CK T1040
  Password / Offline Analysis   MITRE ATT&CK T1110
  ARP Spoofing / MitM           MITRE ATT&CK T1557.002
  KRACK                         NIST NVD CVE-2017-13077
  KRACK Technical Background    CERT/CC VU#228519; Vanhoef & Piessens
  Packet Analysis               Wireshark Documentation
  Wireless Lab Tools            Aircrack-ng Documentation
  Wireless Networking           IEEE 802.11

------------------------------------------------------------------------

## ⚖️ Academic & Ethical Use

Seluruh referensi dan teknik dalam repository ini digunakan untuk
**kepentingan akademik, pembelajaran Cyber Threat Intelligence, dan
pengujian pada lingkungan yang memiliki izin**. Pengujian keamanan tidak
boleh dilakukan terhadap jaringan atau perangkat pihak lain tanpa
otorisasi.
