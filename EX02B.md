# Norm 1 Normalization Process For Veterinary Office
## Each Table Contains a Single Theme , Each Record Is Unique
R1 = PetName (PetType, PetBreed, PetDOB, OwnersLastName, OwnersFirstName, OwnerPhone, OwnerEmail, Service, Date, Charge)

# Norm 2 PrimaryKey Found

R12a = **PetName** (PetType, PetBreed, PetDOB, OwnersLastName, **OwnersFirstName**, OwnerPhone, OwnerEmail, Service, Date, Charge)

R12ab= PetName (PetType, PetBreed, PetDOB, PetID) |
OwnersFirstName(OwnersLastName, OwnerPhone, OwnerEmail, OwnerID) |
Service (Date, Charge,ServiceID)

# Norm 3 ID Relations 

R13b = PetName (PetID, PetType, PetBreed, PetDOB) |
OwnersFirstName(OwnerID, OwnersLastName, OwnerPhone, OwnerEmail, PetID) |
Service (ServiceID,Date, Charge, PetID,OwnerID)
