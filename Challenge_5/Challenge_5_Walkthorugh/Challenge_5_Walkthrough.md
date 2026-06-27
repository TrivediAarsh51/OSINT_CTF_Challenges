# Challenge_5_Walkthrough

## Objective

Determine the **birthplace of the primary suspect** by correlating:

- A hotel image containing hidden GPS coordinates
    
- A separate image of a suspected operative
    

The final flag is the suspect’s **birthplace in the format:**

```
City-District-Country
```

---

## Step 1 – Understand the Challenge

Players are given two key artifacts:

1. An image of a hotel following a terrorist attack
2. An image of a suspected operative linked to the incident

The challenge is designed as a **dual-path investigation**, where both forensic and OSINT approaches lead to the same conclusion.

---

## Step 2 – Extract GPS Coordinates from the Hotel Image

Since this is a forensic investigation, players should inspect the image metadata using a tool such as **ExifTool**.

```bash
exiftool hotel.jpg
```

![[Pasted image 20260625234106.png]]

Inside the metadata, GPS information is present:

```bash
GPS Latitude : 30 deg 52' 52.70" N  
GPS Longitude : 73 deg 35' 58.73" E
```

(Values may appear in DMS format depending on the tool used.)

---

## Step 3 – Convert Coordinates to a Location

Players should enter the coordinates into a mapping service:

```bash
30.8813050373722 , 73.5996462544583
```

![[Pasted image 20260625234143.png]]

This reveals the **geographical region associated with the attack site**, pointing to a location in Punjab, Pakistan.

---

## Step 4 – Analyze the Suspect Image

The second image shows a suspected operative connected to the attack.

Players should:

- Visually analyze the individual
    
- Use OSINT techniques (reverse image search, contextual clues)
    
- Associate the suspect with the same regional network identified via GPS
    

This confirms that both evidence sources point toward the same operational area.

---

## Step 5 – Correlate Intelligence

By combining both findings:

- GPS metadata → operational region of the attack
    
- Suspect image → individual linked to that region
    

Players can identify the suspect and trace background intelligence records.

This leads to the suspect’s **biographical origin data**.

---

## Step 6 – Final Answer (Flag)

The confirmed birthplace of the suspect is:

```
Renala-Khurd-Okara-Pakistan
```

---

## Final Flag Format

```
Flag{Renala-Khurd-Okara-Pakistan}
```

---

## Notes

- GPS data alone is not sufficient — it only provides operational context.
    
- The suspect image is essential for confirming the correct intelligence profile.
    
- Final answer must match the exact format: City-District-Country


## References

- https://www.opensanctions.org/entities/Q3920972/
- https://jamestown.org/the-mastermind-of-mayhem-in-mumbai-a-profile-of-lashkar-e-taibas-zaki-ur-rahman-lakhvi/
- https://www.mha.gov.in/en/page/individual-terrorists-under-uapa
- https://www.satp.org/terrorism-update/mumbai-attack-mastermind-zakiur-rehman-lakhvi-granted-bail













