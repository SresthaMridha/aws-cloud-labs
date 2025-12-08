# IAM Lab Report – Users, Groups, and Policies

## Overview
This lab focused on exploring and managing AWS IAM identities. I worked with pre-created users, groups, and permission policies to understand how access control is structured and enforced within an AWS environment.

## Objectives
- Review existing IAM users and their assigned permissions  
- Explore groups and understand the policies attached to them  
- Analyze managed and inline policies  
- Assign users to groups based on a business access model  
- Verify permission inheritance through group membership  

## Environment Summary
The environment included three IAM users and three groups with predefined permission sets.  
- The support groups used AWS-managed read-only policies.  
- The admin group used a custom inline policy for EC2 administrative actions.  

## Work Performed

### 1. Exploration Phase
I reviewed each user and confirmed that none had direct permissions. I then inspected the groups and examined the attached policies. This helped me understand the difference between:
- **Managed policies** (reusable, maintained by AWS)
- **Inline policies** (custom permissions tied to a specific group or user)

During this review, I also revisited the IAM policy structure, focusing on actions, effects, and resource scopes.

### 2. User Assignment Phase
I attached users to groups according to a business scenario involving S3 support, EC2 support, and EC2 administration. After adding each user to their group, I verified the assigned permissions through the console to confirm proper inheritance.

### 3. Review and Validation
I ensured each group contained the correct user and validated that the access model matched the intended job functions. This step reinforced how IAM simplifies permission management by leveraging groups instead of assigning permissions individually.

## Key Learnings
- Group-based permission management is scalable and reduces administrative overhead.  
- Managed policies provide safe, consistent permission sets suitable for common use cases.  
- Inline policies allow for precise control when unique access requirements exist.  
- Understanding IAM policy structure is essential for enforcing least privilege.  
- Permission inheritance is a core mechanism for managing access efficiently across users.

## Conclusion
This lab strengthened my understanding of IAM fundamentals and demonstrated how user access is designed and maintained in real AWS environments. It provided a practical foundation for building secure architectures and preparing for more advanced cloud administration tasks.
