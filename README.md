# Reviewing-Unallocated-Space-Extracting-Data-with-Tools-Digital-Investigation-Processes
## AIM:
To review unallocated space in a disk image, extract data using forensic tools, and understand the digital investigation process.
## REQUIREMENTS
- Autopsy or FTK Imager
- Sleuth Kit (TSK)
- Hex Editor (e.g., HxD)
- Operating System: Windows 10/11 or Linux (Kali preferred)
## ARCHITECTURE DIAGRAM
```mermaid
flowchart TD
    A[Disk Image / Physical Drive] --> B[Load into Autopsy or Sleuth Kit]
    B --> C[Identify Unallocated Space]
    C --> D[Scan for Data Signatures]
    D --> E[Carve and Recover Files]
    E --> F[Analyze Recovered Data]
    F --> G[Document Findings in Report]
```
## DESIGN STEPS:
### Step 1 (Acquire Evidence Image):
- Obtain the disk image in ```.dd``` or ```.E01``` format from a trusted forensic acquisition process.
- Verify hash values (MD5/SHA256) to maintain integrity.

### Step 2(Load Image into Forensic Tool):
- Open Autopsy or FTK Imager.
- Create a new case and add the evidence image.

### Step 3(Locate Unallocated Space):
- Navigate to the partition structure view.
- Identify sectors not assigned to any partition (unallocated).
### Step 4(Analyze & Carve Data):
- Use built-in data carving tools to search for file signatures (JPEG, DOCX, PDF, etc.).
- Preview carved files for relevance.
  
## PROGRAM:
| Step | Action                     | Tool Used                   | Output                       |
| ---- | -------------------------- | --------------------------- | ---------------------------- |
| 1    | Load disk image            | Autopsy / FTK Imager        | Partition & unallocated view |
| 2    | Identify unallocated space | Autopsy File System View    | Sector ranges                |
| 3    | Data carving               | Autopsy Data Carving Module | Recovered files              |
| 4    | Export evidence            | Autopsy Export Option       | File copies for analysis     |


## OUTPUT:
Unallocated Space Analysis and Extracted Data Report
<img width="1600" height="900" alt="df-1" src="https://github.com/user-attachments/assets/0e9ae4fd-f67a-47fb-b220-162f3cee7a29" />
<img width="1600" height="898" alt="df-2" src="https://github.com/user-attachments/assets/6245f65f-4e45-429e-aa27-0aac04e9aff1" />
<img width="1600" height="899" alt="df-4" src="https://github.com/user-attachments/assets/ce7a5d21-87a0-4b4e-8dd7-7aaeebd16a9f" />
<img width="1600" height="899" alt="df-5" src="https://github.com/user-attachments/assets/d75d5023-147a-4832-9e9c-cb9bb8a0d9ea" />
<img width="1600" height="779" alt="df-6" src="https://github.com/user-attachments/assets/a090453b-70d1-4e85-a38e-19ab85c13472" />
<img width="1600" height="740" alt="df-7" src="https://github.com/user-attachments/assets/f55b6c7e-6858-429a-910e-108c1ebdfe5a" />



## RESULT:
The unallocated space was successfully analyzed, data was extracted, and the digital investigation process was followed effectively.

