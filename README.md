# Disk_Imaging


Creating a Forensically Sound Disk Image 

This project demonstrates how to safely acquire a forensically sound disk image from a suspect Windows 11 virtual machine using three industry‑standard tools: dc3dd, ewfacquire, and Guymager. All imaging and verification steps are performed from a separate Tsurugi Linux forensic VM to ensure evidence integrity.



Purpose of the Lab

The goal of this module is to practice proper forensic methodology, including:

 Imaging a disk without altering evidence  
 Using multiple acquisition tools and formats  
 Verifying image integrity with cryptographic hashes  
 Documenting each step clearly and repeatably  



Environment

  Suspect VM:Windows 11 (powered off before imaging)  
  Forensic VM: Tsurugi Linux  
  Disk Type: VMDK (attached as a secondary read‑only disk)  
  Tools Used: dc3dd, ewfacquire (E01), Guymager  



Imaging Methods Used

1. dc3dd (Raw Image – .dd)
 Creates a bit‑for‑bit raw image  
 Hashes generated: MD5, SHA1, SHA256, SHA512  
 Metadata stored separately in a log file  

2. ewfacquire (E01 Format)
 Produces Expert Witness Format (E01)  
 Includes embedded metadata (case info, examiner, description)  
 Verified using `ewfverify`  

3. Guymager (GUI Tool)
 Easy graphical interface  
 Supports MD5 + SHA256 hashing  
 Generates detailed acquisition logs  


Verification
For each imaging method:

 Hashes of the source disk were recorded  
 Hashes of the image file were recorded  
 Values were compared to confirm forensic integrity  
 Logs and screenshots were saved as evidence  


 Deliverables Included

 Imaging steps for all three tools  
 Hash values for each image  
 Verification logs and screenshots  
 Reflection answers comparing tools and methodology  



Key Learning Outcomes

 Understanding what makes an image “forensically sound”  
 Safely acquiring evidence in read‑only mode  
 Using multiple forensic imaging tools  
 Verifying integrity with cryptographic hashing  
 Documenting procedures for chain of custody  

