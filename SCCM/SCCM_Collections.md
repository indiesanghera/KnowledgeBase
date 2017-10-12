# SCCM_Collections

## Clients

### Collection for all Workstations.

```sql
select SMS_R_SYSTEM.ResourceID, SMS_R_SYSTEM.ResourceType, SMS_R_SYSTEM.Name, SMS_R_SYSTEM.SMSUniqueIdentifier,SMS_R_System.OperatingSystemNameandVersion,
SMS_R_SYSTEM.ResourceDomainORWorkgroup, SMS_R_SYSTEM.Client
from SMS_R_System where SMS_R_System.OperatingSystemNameandVersion like "Microsoft Windows NT Workstation%"
```

### Collection of All Windows 10 Creators Update (1703)

```sql
select * from  SMS_R_System inner join SMS_G_System_OPERATING_SYSTEM on SMS_G_System_OPERATING_SYSTEM.ResourceId = SMS_R_System.ResourceId where SMS_G_System_OPERATING_SYSTEM.BuildNumber = "15063"
```

### Collection of All Windows 10 Aniversary Update (1607)

```sql
select * from  SMS_R_System inner join SMS_G_System_OPERATING_SYSTEM on SMS_G_System_OPERATING_SYSTEM.ResourceId = SMS_R_System.ResourceId where SMS_G_System_OPERATING_SYSTEM.BuildNumber = "14393"
```

### Collection of All Windows 10 November Update (1511)

```sql
select * from  SMS_R_System inner join SMS_G_System_OPERATING_SYSTEM on SMS_G_System_OPERATING_SYSTEM.ResourceId = SMS_R_System.ResourceId where SMS_G_System_OPERATING_SYSTEM.BuildNumber = "10586"
```

