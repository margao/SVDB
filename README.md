# SVDB
Shadowverse Database

Website built with HTML5/CSS/Javascript/JQuery/PHP utilizing a MySQL database.

# Relation Tables, Types & Domain, and Functional Dependencies

FollowerCard ( cardID, cardname, cardset, cardclass, rarity, ppcost, flavortext, atk, def, EvolAtk, EvolDef, attribute, abilityID, soundID, artID)
Where FollowerCard.attributeID = Attribute.attributeID
FollowerCard.abilityID = Ability.abilityID
Followercard.soundID = Sound.soundID
Followercard.artID = Artwork.artID
Types and Domain:
cardID INT(11)
cardname VARCHAR(255)
cardset VARCHAR(255)
cardclass VARCHAR(255) from string set { Bloodcraft, Swordcraft,
Shadowcraft, Havencraft, Dragoncraft, Forestcraft, Runecraft,
Neutral }
rarity VARCHAR(255) from string set { Bronze, Silver, Gold,
Legendary }
ppcost INT(4)
flavortext VARCHAR(255)
atk INT(4)
def INT(4)
EvolAtk INT(4)
EvolDef INT(4)
attribute VARCHAR(255)
abilityID INT(4)
soundID INT(4)
artID INT(4)
Functional Dependencies
cardID -> cardname, cardset, cardclass, rarity, ppcost, flavortext, atk, def, EvolAtk, EvolDef, attribute , abilityID, soundID, artID

AmuletCard ( cardID, cardname, cardset, cardclass, rarity, ppcost, flavortext, type, attribute, artID, abilityID,)
Where PermanentAmuletCard.artID = Artwork.artID
PermanentAmuletCard.abilityID = AmuletAbility.abilityID
Types and Domain:
cardID INT(11)
cardname VARCHAR(255)
cardset VARCHAR(255)
cardclass VARCHAR(255) from string set { Bloodcraft, Swordcraft,
Shadowcraft, Havencraft, Dragoncraft, Forestcraft, Runecraft,
Neutral }
rarity VARCHAR(255) from string set { Bronze, Silver, Gold,
Legendary }
ppcost INT(4)
flavortext VARCHAR(255)
type VARCHAR(255) from string set { Permanent, Cooldown }
attribute VARCHAR(255)
artID INT(4)
abilityID INT(4)
Functional Dependencies
cardID -> cardname, cardset, cardclass, rarity, ppcost, flavortext, type, attribute, artID, abilityID,

SpellCard ( cardID, cardname, cardset, cardclass, rarity, ppcost, abilityID, flavortext, artID)
Where SpellCard.soundID = Sound.soundID
SpellCard.artID = Artwork.artID
SpellCard.abilityID = SpellAbility.abilityID
Types and Domain:
cardID INT(11)
cardname VARCHAR(255)
cardset VARCHAR(255)
cardclass VARCHAR(255) from string set { Bloodcraft, Swordcraft,
Shadowcraft, Havencraft, Dragoncraft, Forestcraft, Runecraft,
Neutral }
rarity VARCHAR(255) from string set { Bronze, Silver, Gold,
Legendary }
ppcost INT(4)
flavortext VARCHAR(255)
abilityID INT(4)
artID INT(4)
Functional Dependencies
cardID -> cardname, cardset, cardclass, rarity, ppcost, abilityID, flavortext, artID

FollowerArtwork ( artID, artworkURL ) Types and Domain:
artID NUMBER(max) artworkURL VARCHAR(255)
Functional Dependencies
artID -> artworkURL

SpellArtwork ( artID, artworkURL) Types and Domain:
artID NUMBER(max) artworkURL VARCHAR(255)
Functional Dependencies
artID -> artworkURL

AmuletArtwork ( artID, artworkURL)
Types and Domain:
artID NUMBER(max) artworkURL VARCHAR(255)
Functional Dependencies
artID -> artworkURL

Sound ( soundID, soundURL) Types and Domain:
soundID NUMBER(max) soundURL VARCHAR(255)
Functional Dependencies
soundID -> soundURL

SpellAbility ( abilityID, abilityText) Types and Domain:
abilityID NUMBER(max) abilityText VARCHAR(255)
Functional Dependencies
abilityID -> abiltyText

FollowerAbility ( abilityID, abilityText) Types and Domain:
abilityID NUMBER(max) abilityText VARCHAR(255)
Functional Dependencies
abilityID -> abiltyText

AmuletAbility ( abilityID, abilityText) Types and Domain:
abilityID NUMBER(max) abilityText VARCHAR(255)
Functional Dependencies
abilityID -> abiltyText

