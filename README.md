A CircleCI orb that scans a given web address using arachni-scanner and then passes or fails the job based on the severity of vulnerabilities that are found.

    version 2.1
    orbs:
      arachni: aniemack/arachni@1.2.3
    
    workflows:
      arachni_scan:
        jobs:
          - arachni/scan:
              site_name: 'https://example.com'
              severity: (Select one from 'High' 'Medium' 'Low' or 'Informational')
