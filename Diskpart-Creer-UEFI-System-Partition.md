  # Preparer un Disque (HDD, SSD, M2) 
  + Creer 
    + UEFI-System-Partition
      + Instruction pour Diskpart
        + list disk
        + select disk X
        + convert gpt
        + create partition efi size=100
        + format quick fs=fat32 label="System"
        + assign letter="S"
        + create partition msr size=16
        + create partition primary 
        + shrink minimum=639
        + format quick fs=ntfs label="Windows"
        + assign letter="W"
        + create partition primary
        + format quick fs=ntfs label="Windows RE tools"
        + assign letter="T"
        + set id=de94bba4-06d1-4d40-a16a-bfd50179d6ac
        + gpt attributes=0x8000000000000001
        + list volume
        + exit
