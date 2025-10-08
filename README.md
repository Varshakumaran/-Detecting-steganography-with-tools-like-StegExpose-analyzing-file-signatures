# Detecting-steganography-with-tools-like-StegExpose-analyzing-file-signatures
## AIM:
To detect hidden data using steganography detection tools like StegExpose and analyze file signatures for authenticity and manipulation.
## Requirements:
- **Operating System:** Linux / Windows
- **Tools:**
    - StegExpose (Java-based tool)
    - Hex Editor (e.g., xxd, HxD)
    - File command (Linux) or TrID (Windows)
- **Sample files:**
    - Suspected stego files (.jpg, .png, .wav)
    - Clean reference files
## ARCHITECTURE DIAGRAM:
```mermaid
flowchart TD
    A[Input File: JPG/PNG/WAV] --> B[File Signature Analysis]
    B --> C{Signature Match?}
    C -- Yes --> D[Pass to StegExpose]
    C -- No --> E[File Tampered / Mismatch]
    D --> F[StegExpose Detection: Suspicious or Clean]
    F --> G[Report Findings]
```

## DESIGN STEPS:
### Step 1:
Install StegExpose or use the JAR version to detect steganography in image files.

### Step 2:
Run StegExpose on a directory of suspected image files using the command:

### Step 3:
Analyze file signatures using tools like file, binwalk, or xxd to check for inconsistencies or embedded content.

## PROGRAM:
**Check file type**
```bash
file suspect.jpg
```
or view magic bytes:
```
xxd suspect.jpg | head
```
**Run StegExpose**
```bash
java -jar StegExpose.jar suspect.jpg
```
## OUTPUT:
List of Images with Steganography Detection Scores and File Signature Details

<img width="1035" height="556" alt="image" src="https://github.com/user-attachments/assets/34642f50-da43-4db3-84c5-a620dcf62f07" />

<img width="1035" height="542" alt="image" src="https://github.com/user-attachments/assets/1244ce50-c678-4f15-82a4-cce7cf2b7291" />

<img width="1013" height="533" alt="image" src="https://github.com/user-attachments/assets/c4b608af-85d6-4a6c-a970-aaa999c7c5d7" />

<img width="1030" height="542" alt="image" src="https://github.com/user-attachments/assets/8a912e5c-50e1-46cb-9138-414e734e8c35" />

<img width="1029" height="528" alt="image" src="https://github.com/user-attachments/assets/1fef6b32-a531-47e3-a5b3-1417ec4dc67f" />

<img width="1020" height="550" alt="image" src="https://github.com/user-attachments/assets/89967ad9-66fd-4130-8565-f37eb8877532" />

<img width="1025" height="544" alt="image" src="https://github.com/user-attachments/assets/b10c5a55-8d0d-4fbf-b046-b5a7554719db" />

## RESULT:
Hidden data was successfully detected and file signatures were analyzed for irregularities.
