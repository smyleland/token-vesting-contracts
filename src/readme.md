# Requirements for Vesting

## Token
Total supply of 1,000,000,000 Smyle Tokens.

## Cliff Vesting Period
Angel investors get 1-year cliff and 5-year vesting schedule.
The cliff period starts from 1 March 2023. Angel investors will receive the first 20% of the tokens on 1 March 2024.

## Vesting Duration
20% of the tokens will be vested every 12 months for 5 years.

2023-03-01  2024-03-01  2025-03-01  2026-03-01  2027-03-01  2028-03-01
0 mo        12 mo       24 mo       36 mo       48 mo       60 mo
.............................................................
^           ^           ^           ^           ^           ^
Start       1st vest    2nd vest    3rd vest    4th vest    5th vest
0%          20%         20%         20%         20%         20%

## Token Features (deprecated)
1. Max token per wallet 1% of circulating supply
2. Tax x% and Tax adjustment period setting 
3. Max transaction trading x% of circulating supply
4. Lockup period (NO Trade) for all token
5. No short sell (#days)

# Vesting Smart Contract Features

## External Methods

### Only Owner
1. createVestingSchedule()
   Call this method to create vesting schedule for each beneficiary. One beneficiary may have more than one schedule.
2. revoke()
3. withdraw()
4. computeReleasableAmount()

### Public
1. release()
   Call this method to release eligible vested amount to beneficiary.
2. getVestingSchedulesCountByBeneficiary()
3. getVestingIdAtIndex()
4. getVestingScheduleByAddressAndIndex()
5. getVestingSchedulesTotalAmount()
6. getToken()
7. getVestingSchedulesCount()
8. getVestingSchedule()
9. getWithdrawableAmount()
10. computeNextVestingScheduleIdForHolder()
11. getLastVestingScheduleForHolder()
12. computeVestingScheduleIdForAddressAndIndex()

# Vesting Schedules

## Template For Investors
_beneficiary = {wallet_address_of_an_investor}
_start = The start timestamp to start the token cliff vesting. This is a Unix epoch timestamp.
_cliff = The cliff period from the start timestamp in seconds e.g. 1 year = 365 days = 31,536,000 seconds
_duration = The vesting duration including the cliff period in seconds e.g. 5 years = 365 * 5 days = 157,680,000 seconds
_slicePeriodSeconds = The time between each vest within the vesting duration in seconds e.g. 1 year = 365 days = 31,536,000 seconds
_revocable = false, Can this vesting schedule be revocable?
_amount = Amount of tokens to cliff-vest in each schedule

### Angel #1
Schedule: start == 2023-03-01 (GMT+7), cliff == 1 year, vesting duration == 5 years, slice period == 1 year
_beneficiary = {wallet_address_of_an_investor}
_start = 1677603600
_cliff = 31536000
_duration = 157680000
_slicePeriodSeconds = 31536000
_revocable = false
_amount = 1500000

### Angel #2
Schedule: start == 2023-03-01 (GMT+7), cliff == 1 year, vesting duration == 5 years, slice period == 1 year
_beneficiary = {wallet_address_of_an_investor}
_start = 1677603600
_cliff = 31536000
_duration = 157680000
_slicePeriodSeconds = 31536000
_revocable = false
_amount = 750000

### Angel #3
Schedule: start == 2023-03-01 (GMT+7), cliff == 1 year, vesting duration == 5 years, slice period == 1 year
_beneficiary = {wallet_address_of_an_investor}
_start = 1677603600
_cliff = 31536000
_duration = 157680000
_slicePeriodSeconds = 31536000
_revocable = false
_amount = 750000

### Angel #4
Schedule: start == 2023-03-01 (GMT+7), cliff == 1 year, vesting duration == 5 years, slice period == 1 year
_beneficiary = {wallet_address_of_an_investor}
_start = 1677603600
_cliff = 31536000
_duration = 157680000
_slicePeriodSeconds = 31536000
_revocable = false
_amount = 1200000

### Angel #5
Schedule: start == 2023-03-01 (GMT+7), cliff == 1 year, vesting duration == 5 years, slice period == 1 year
_beneficiary = {wallet_address_of_an_investor}
_start = 1677603600
_cliff = 31536000
_duration = 157680000
_slicePeriodSeconds = 31536000
_revocable = false
_amount = 300000

### Angel #6
Schedule: start == 2023-03-01 (GMT+7), cliff == 1 year, vesting duration == 5 years, slice period == 1 year
_beneficiary = {wallet_address_of_an_investor}
_start = 1677603600
_cliff = 31536000
_duration = 157680000
_slicePeriodSeconds = 31536000
_revocable = false
_amount = 1500000

### Angel #7
Schedule: start == 2023-03-01 (GMT+7), cliff == 1 year, vesting duration == 5 years, slice period == 1 year
_beneficiary = {wallet_address_of_an_investor}
_start = 1677603600
_cliff = 31536000
_duration = 157680000
_slicePeriodSeconds = 31536000
_revocable = false
_amount = 1500000

### Angel #8
Schedule: start == 2023-03-01 (GMT+7), cliff == 1 year, vesting duration == 5 years, slice period == 1 year
_beneficiary = {wallet_address_of_an_investor}
_start = 1677603600
_cliff = 31536000
_duration = 157680000
_slicePeriodSeconds = 31536000
_revocable = false
_amount = 1500000

### Angel #9
Schedule: start == 2023-03-01 (GMT+7), cliff == 1 year, vesting duration == 5 years, slice period == 1 year
_beneficiary = {wallet_address_of_an_investor}
_start = 1677603600
_cliff = 31536000
_duration = 157680000
_slicePeriodSeconds = 31536000
_revocable = false
_amount = 1500000

### Angel #10
Schedule: start == 2023-03-01 (GMT+7), cliff == 1 year, vesting duration == 5 years, slice period == 1 year
_beneficiary = {wallet_address_of_an_investor}
_start = 1677603600
_cliff = 31536000
_duration = 157680000
_slicePeriodSeconds = 31536000
_revocable = false
_amount = 750000

### Angel #11
Schedule: start == 2023-03-01 (GMT+7), cliff == 1 year, vesting duration == 5 years, slice period == 1 year
_beneficiary = {wallet_address_of_an_investor}
_start = 1677603600
_cliff = 31536000
_duration = 157680000
_slicePeriodSeconds = 31536000
_revocable = false
_amount = 600000

### Angel #12
Schedule: start == 2023-03-01 (GMT+7), cliff == 1 year, vesting duration == 5 years, slice period == 1 year
_beneficiary = {wallet_address_of_an_investor}
_start = 1677603600
_cliff = 31536000
_duration = 157680000
_slicePeriodSeconds = 31536000
_revocable = false
_amount = 300000

### Angel #13
Schedule: start == 2023-03-01 (GMT+7), cliff == 1 year, vesting duration == 5 years, slice period == 1 year
_beneficiary = {wallet_address_of_an_investor}
_start = 1677603600
_cliff = 31536000
_duration = 157680000
_slicePeriodSeconds = 31536000
_revocable = false
_amount = 600000

### Angel #14
Schedule: start == 2023-03-01 (GMT+7), cliff == 1 year, vesting duration == 5 years, slice period == 1 year
_beneficiary = {wallet_address_of_an_investor}
_start = 1677603600
_cliff = 31536000
_duration = 157680000
_slicePeriodSeconds = 31536000
_revocable = false
_amount = 1500000

## For Employees
TBD