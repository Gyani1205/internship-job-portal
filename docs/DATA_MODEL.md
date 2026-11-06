# Data Model

## Collection 1: jobs

Stores every internship or job listing.

| Field | Type | Required? | Example | Purpose |
|---|---|---|---|---|
| title | String | Yes | Frontend Developer Intern | Name of the position |
| company | String | Yes | TechNova | Company offering the position |
| location | String | Yes | Remote | Where the work happens |
| type | String | Yes | Internship | Either "Internship" or "Full-time" |
| description | String | Yes | Develop responsive web pages | Full details of the role |
| salary | String | No | ₹15,000/month | Salary or internship stipend |
| skills | Array of Strings | No | HTML, CSS, JavaScript | Skills required for the position |
| createdAt | Date | Auto | 2026-11-05 | When the listing was created |

## Collection 2: applications

Stores every application a job seeker submits.

| Field | Type | Required? | Example | Purpose |
|---|---|---|---|---|
| jobId | ObjectId | Yes | ID of a job | Links the application to a job |
| applicantName | String | Yes | Gyaneswari | Name of the applicant |
| email | String | Yes | student@example.com | Applicant's email address |
| phone | String | Yes | 9876543210 | Applicant's contact number |
| resumeLink | String | Yes | https://example.com/resume | Link to the applicant's resume |
| coverNote | String | No | I am interested in this role | Applicant's introduction |
| createdAt | Date | Auto | 2026-11-05 | When the application was submitted |

## Notes

The jobs collection stores all available job and internship details. The applications collection stores information about people who apply for those jobs. The jobId field connects each application to the specific job listing it belongs to. This helps the admin identify which job each applicant has applied for.