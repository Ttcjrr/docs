---
title: About private networking with GitHub-hosted runners
shortTitle: About private networking
intro: '{% data reusables.actions.private-networking-intro %}'
versions:
  fpt: '*'
  ghes: '*'
  ghec: '*'
type: overview
topics:
  - Actions
  - Action development
  - Azure Virtual Network
  - Administrator
  - Developer
  - CI
  - CD
---

{% data reusables.actions.enterprise-github-hosted-runners %}

## About {% data variables.product.prodname_dotcom %}-hosted runners networking

{% data reusables.actions.about-private-networking-github-hosted-runners %}

There are a few different approaches you could take to configure this access, each with different advantages and disadvantages.

## Using an API Gateway with OIDC

{% data reusables.actions.private-networking-oidc-intro %} For more information, see "[AUTOTITLE](/actions/using-github-hosted-runners/connecting-to-a-private-network/using-an-api-gateway-with-oidc)."

## Using WireGuard to create a network overlay

{% data reusables.actions.private-networking-wireguard-intro %} For more information, see "[AUTOTITLE](/actions/using-github-hosted-runners/connecting-to-a-private-network/using-wireguard-to-create-a-network-overlay)."

{% ifversion actions-private-networking-azure-vnet %}

## Using an Azure Virtual Network (VNET)

{% data reusables.actions.azure-vnet-network-configuration-intro %}

{% ifversion fpt %}

Organization owners using the {% data variables.product.prodname_team %} plan can configure {% data variables.product.company_short %}-hosted runners at the organization level. For more information, see "[AUTOTITLE](/organizations/managing-organization-settings/about-azure-private-networking-for-github-hosted-runners-in-your-organization)."

Enterprise owners using {% data variables.product.prodname_ghe_cloud %} can configure Azure private networking at the enterprise level. For more information about upgrading to {% data variables.product.prodname_ghe_cloud %}, see "[AUTOTITLE](/billing/managing-the-plan-for-your-github-account/upgrading-your-accounts-plan)."

For more information about configuring Azure private networking at the enterprise level, see "[AUTOTITLE](/enterprise-cloud@latest/admin/configuration/configuring-private-networking-for-hosted-compute-products/about-azure-private-networking-for-github-hosted-runners-in-your-enterprise)."

{% endif %}

{% ifversion ghec %}

Enterprise owners can configure Azure private networking at the enterprise level. For more information, see "[AUTOTITLE](/enterprise-cloud@latest/admin/configuration/configuring-private-networking-for-hosted-compute-products/about-azure-private-networking-for-github-hosted-runners-in-your-enterprise)."

Organization owners for organizations in an enterprise can configure {% data variables.product.company_short %}-hosted runners at the organization level. For more information, see "[AUTOTITLE](/organizations/managing-organization-settings/about-azure-private-networking-for-github-hosted-runners-in-your-organization)."

{% endif %}

{% endif %}
