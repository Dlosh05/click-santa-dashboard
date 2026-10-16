# Click Photo Ops — Santa Ticket Dashboard

Static website for counting Photo with Santa packages from a Will Call CSV report.

## Deploy to Render

1. Create a new GitHub repository, e.g. `click-santa-dashboard`.
2. Upload `index.html` and `render.yaml` to the repository root.
3. In Render, select **New > Blueprint** and connect the GitHub repository.
4. Review the proposed `click-santa-dashboard` static service and deploy it.
5. Open the `onrender.com` address Render provides.

Alternatively, create a **New > Static Site** in Render, connect the repository, set build command to `echo ready` and publish directory to `.`.

## Use

Upload your Will Call CSV, then select an event date. The dashboard filters ticket type names containing `Photo with Santa`, excludes canceled/refunded/voided/deleted statuses, and sums the Quantity column for each scheduled start/end time. Download the summary as CSV or print the report.

The CSV is read locally in the browser; it is not sent to a server. No database, API key, or environment variables are required.
