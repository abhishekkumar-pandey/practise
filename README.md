<!DOCTYPE html>
<html>
<head>
    <title>POR Chatbot Test</title>
    <style>
         #contentBox {MARGIN-LEFT: 10px;}
			#contentBox {PADDING-TOP: 0px; }
			#contentRow {PADDING-TOP: 0px; }
			.ms-rtestate-field p, p.ms-rteElement-P{margin:-20px 0px 10px 0px;}
			.ms-breadcrumb-top { margin-top:-20px;}
			.ms-rte-layoutszone-inner{margin-top:-20px;}
			#O365_MainLink_Settings {display:none;}
			#O365_MainLink_Help_container {display:none;}
			#s4-titlerow {
			margin-top:0px;
			margin-bottom:-15px;
			}
			#s4-ribbonrow {
			display:none;
			}
			#sideNavBox{
			display:none;
			}
			.ms-core-pageTitle {display:none;}
			.ms-siteicon-img {
			display:none;
			}
			.ms-srch-sb {
			display:none;
			}
			.ms-listMenu-editLink {
			display:none;
			}
			.ms-navedit-editLinksText{
			display:none;
			}
			#s4-ribbonrow, .ms-cui-topBar2, .s4-notdlg, .s4-pr s4-ribbonrowhidetitle, .s4-notdlg noindex, #ms-cui-ribbonTopBars,  #s4-pr s4-notdlg s4-titlerowhidetitle, #s4-leftpanel-content {display:none !important;}
			.s4-ca {margin-left:0px !important; margin-right:0px !important;}
			.menu-item-text {font-size:15px;margin-left:90px;}
        body {
            font-family: Arial, sans-serif;
            margin: 30px;
        }

        input {
            width: 500px;
            padding: 8px;
        }

        button {
            padding: 8px 15px;
        }

        #result {
            margin-top: 20px;
            white-space: pre-wrap;
            border: 1px solid #ccc;
            padding: 15px;
        }
    </style>
</head>
<body>

    <h2>POR Chatbot Test</h2>

    <input
        id="question"
        type="text"
        placeholder="Example: Show PO 9200141292"
    >

    <button onclick="askBot()">Ask</button>

    <div id="result"></div>

<script>

async function askBot() {

    const question =
        document.getElementById("question").value.trim();

    const result =
        document.getElementById("result");

    const match =
        question.match(/\d{10}/);

    if (!match) {
        result.innerHTML =
            "Please enter: Show PO 9200141292";
        return;
    }

    const poNumber = match[0];

    result.innerHTML = "Searching...";

    const apiUrl =
        "https://hclo365nam.sharepoint.com/sites/HPE-teams-BPTOOL_NCTG" +
        "/_api/web/lists/getbytitle('PORLISTHCL')/items" +
        "?$filter=PO_Number eq '" + poNumber + "'";

    try {

        const response = await fetch(apiUrl, {
            headers: {
                "Accept": "application/json;odata=nometadata"
            },
            credentials: "include"
        });

        const data = await response.json();

        if (!data.value || data.value.length === 0) {
            result.innerHTML =
                "No records found for PO " + poNumber;
            return;
        }

        const item = data.value[0];

        result.innerHTML =
`
PO Number: ${item.PO_Number || "N/A"}

PR Number: ${item.PR_Number || "N/A"}

Vendor:
${item.Vendor_Name || "N/A"}

Customer:
${item.Customer_Name || "N/A"}

Project:
${item.Project_Name || "N/A"}

Country:
${item.Project_Country || "N/A"}

Status:
${item.Flowstatus || "N/A"}
`;

    }
    catch (e) {

        result.innerHTML =
            "Error:<br>" + e.message;
    }
}

</script>

</body>
</html>
