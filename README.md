# phonenumbers_details
import phonenumbers
from phonenumbers import carrier, geocoder, timezone

mobileNo = input("enter Mobile Number with country code:")
mobileNo = phonenumbers.parse(mobileNo)

# get timezone a phone number
print(timezone.time_zones_for_number(mobileNo))

# getting carrier of a phone number
print(carrier.name_for_number(mobileNo, "en"))

# getting region information
print(geocoder.description_for_number(mobileNo, "en"))

# validating a phone number
print("valid Mobile Number :", phonenumbers.is_valid_number(mobileNo))

# checking possibility of Number
print("checking possibility of Number :", phonenumbers.is_possible_number(mobileNo))
