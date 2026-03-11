# Motion system upgrades
### Motivation behind the upgrade
The stock SV07+ uses V-slot roller guides on all three axes.
While inexpensive, this solution tends to be both noisy and mechanically unstable, particularly on the Y axis.

The resulting play in the motion system limits the maximum accelerations and printing speeds that can be achieved reliably.
To improve rigidity and motion quality, I decided to replace the V-roller system on the X and Y axes with linear guides.

## Parts selection

After deciding to upgrade the motion system to linear guides, I considered two possible options:
- MGN9
- MGN12  

MGN9 rails have smaller carriages, which would make them easier to mount on the sides of the 2040 extrusion supporting the heated bed.

However, MGN12 rails provide a significant advantage: the 20 mm carriage width allows their rails to sit securely on a standard V-slot extrusion profile.

Using MGN9 would require printed filler parts to bridge the gap between the rail and the extrusion. This would partially defeat the purpose of the upgrade, which was to improve precision and reduce noise.

For this reason, MGN12 rails were selected.

## Upgrade design

To install the rails on the Y axis, two custom printed parts were designed:
- guide-bed connector
- profile spacer

The spacer provides several millimeters of clearance so that the rail carriage can move freely.

The connector ensures proper mechanical coupling between the heated bed assembly and the linear guide carriage.

### Mechanical requirements

The printed parts used to mount the linear rails had to meet several mechanical and geometrical requirements:

- sufficient stiffness to avoid introducing compliance into the motion system
- dimensional accuracy to ensure correct alignment of the linear rail
- resistance to moderate temperatures from the heated bed
- compatibility with the existing aluminium extrusion frame

### Material selection

Ideally, ABS would have been a more suitable material for these components due to its higher temperature resistance and better long-term mechanical stability.

However, at the time of designing these parts I did not have the capability to reliably print ABS parts. For this reason PETG was selected as a practical alternative.

PETG provides sufficient strength and toughness for the expected loads, while remaining easy to print and dimensionally stable. Given the relatively low mechanical loads and the large contact surfaces of the parts, PETG was considered an adequate material for this application.

## Implementation
### Y-Axis
The final assembly of the Y-axis upgrade is shown below.

<img width="1223" height="657" alt="obraz" src="https://github.com/user-attachments/assets/2961496b-415e-4119-90f1-efc3fc009045" />

The connector includes pockets for M5 nuts to provide durable metal threads for mounting the part to the heated bed plate.
Its ribbed structure increases stiffness and helps mitigate long-term material creep.

The profile spacer is a simpler component that elevates the rail assembly so that the carriage can move freely without interfering with the base extrusion.

Printed parts installed on the printer are shown below.

<img width="497" height="396" alt="obraz" src="https://github.com/user-attachments/assets/60b35c98-c440-4d9b-81b2-918a256cabab" />

<img width="633" height="447" alt="obraz" src="https://github.com/user-attachments/assets/6ef96b24-1862-4501-b4dd-78f858dedec5" />

<img width="2048" height="1536" alt="obraz" src="https://github.com/user-attachments/assets/f06238af-b0da-48b3-b4b1-3a0878bcd8ae" />

### X-Axis
The X axis was upgraded as well, although it did not require additional printed parts.
The rail could be mounted directly to the stock extrusion after drilling mounting holes.

<img width="634" height="352" alt="obraz" src="https://github.com/user-attachments/assets/070d2a46-1432-42b1-823d-1c960816da06" />

## Results

After the upgrade and relubrication of the rails, the printer operated significantly more reliably and noticeably quieter.

The measured input shaper frequencies decreased by approximately 30%, indicating reduced structural vibrations and improved rigidity of the motion system.

