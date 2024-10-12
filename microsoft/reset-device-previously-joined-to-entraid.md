# Reset A Device Previously Joined to Entra ID

> Some of the sources reference Azure Active Directory (AAD).
> AAD was renamed 'Entra ID' by Microsoft.
> I reference Entra ID since it is the name at the time of writing.

If you have devices previously joined to Entra ID, you may need to remove some of the GUIDs from the registry.

1. Remove GUIDs
1. Sysprep with reboot
1. Login with work account
1. Rename PC (sysprep removes existing PC Name)


## References

+ As of July 2024 comments on this ![blog post](https://jocha.se/blog/tech/azure-ad-mdm-intune-error-8018000a) are saying the instructions are still valid.
+ Microsoft Learn ![discussion](https://learn.microsoft.com/en-us/answers/questions/210271/cannot-join-device-to-azure-ad-states-device-is-al) started in December 2020.
+ Microsoft Tech Community ![thread](https://techcommunity.microsoft.com/t5/windows-management/can-t-aad-join-windows-10-quot-administrator-policy-does-not/m-p/2109878) started in February 2021.
