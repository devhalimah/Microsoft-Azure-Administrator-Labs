<h1>Managing Azure Resources Using Azure Powershell</h1>
<h2>Lab scenario</h2>
As the Azure Administrator for your organization, you're to automate the following administration tasks by using Azure PowerShell:
<ul>
  <li>Creating resources groups.</li>
  <li>Creating managed disks.</li>
  <li>Changing the configuration of managed disks.</li>
</ul>

<h2>Solution</h2>
<h3>Step 1: Starting PowerShell session in Azure Cloud Shell</h3>
<ul>
  <li><p><b>Creating storage account:</b></p></li>
<img width="960" alt="image" src="https://github.com/devhalimah/Microsoft-Azure-Administrator-Labs/assets/64546668/2e8f0e38-7ba9-4759-99b4-ee72fdca86aa">

  <li><p><b>PowerShell session started:</b></p></li>
  <img width="960" alt="image" src="https://github.com/devhalimah/Microsoft-Azure-Administrator-Labs/assets/64546668/32ade43a-88c5-4536-ac81-98fdfb348841">
</ul>

----------------------------------------------------------------------------------------------------------
<h3>Step 2: Creating a resource group using Azure PowerShell</h3>
<img width="960" alt="image" src="https://github.com/devhalimah/Microsoft-Azure-Administrator-Labs/assets/64546668/8feb9db8-c563-4894-928e-e32654915828">
<ul>
  <b>From the PowerShell session within Azure Cloud Shell, I ran the following commands as shown above to create a resource group in the same Azure region (West Europe) as the resource group (AZ104_Labs) created in the previous step.</b>
  <p><li>This command gets the azure region ('Location') of the previously created resource group (AZ104_Labs), and assigns it to a variable ($location).
  <pre>$location = (Get-AzResourceGroup -Name AZ104_Labs).Location</pre></li>
  <li>This command sets the new resource group name and assigns it to a variable ($rgName).
  <pre>$rgName = 'new_az104_lab'</pre></li>
  <li>The actual command used to create a new resource group. This command gets the values of the created variables and creates the new resource group.
  <pre>New-AzResourceGroup -Name $rgName -Location $location</pre></li>
</p></ul>

----------------------------------------------------------------------------------------------------------
<h3>Step 3: Creating an Azure managed disk using Azure PowerShell</h3>
