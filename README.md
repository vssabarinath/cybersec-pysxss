CSRF Vulnerability Scanner

This script scans a given URL for potential Cross-Site Request Forgery (CSRF) vulnerabilities by analyzing the elements on the webpage.

How It Works:
   Fetch the Webpage:
   
   Uses requests to retrieve the page's HTML content.
   Handles errors (e.g., invalid URL or network issues). ###Parse HTML Forms:
   Uses BeautifulSoup to find all elements on the page.

Check for CSRF Protection:

    Each form is checked for a hidden field with the name csrf_token (or similar).
    If a form lacks this field, it is flagged as potentially vulnerable.

Output Results:
       Displays the action URL of each potentially vulnerable form and its full HTML structure.
       
Example Usage:

Run the script.
Enter the target URL when prompted.
If vulnerabilities are found, the script lists:
                   Action URL: Where the form submits data.
                   Form HTML: The entire HTML of the vulnerable form.
Notes:

:Modify the csrf_token field name if the target site uses a custom name for CSRF tokens.
:Always have permission before scanning websites, as unauthorized scanning may be illegal.
