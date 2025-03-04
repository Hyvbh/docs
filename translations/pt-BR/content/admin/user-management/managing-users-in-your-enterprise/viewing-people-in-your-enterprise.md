---
title: Visualizar pessoas na sua empresa
intro: 'Para auditar o acesso à utilização de licença de usuário ou de recursos pertencentes à empresa, os proprietários corporativos podem exibir todos os administradores e integrantes da empresa.'
redirect_from:
  - /github/setting-up-and-managing-your-enterprise-account/viewing-people-in-your-enterprise-account
  - /articles/viewing-people-in-your-enterprise-account
  - /github/setting-up-and-managing-your-enterprise/viewing-people-in-your-enterprise
  - /github/setting-up-and-managing-your-enterprise/managing-users-in-your-enterprise/viewing-people-in-your-enterprise
versions:
  ghec: '*'
  ghes: '*'
  ghae: '*'
topics:
  - Enterprise
shortTitle: Visualizar as pessoas na sua empresa
---

## Sobre a lista de pessoas da sua empresa

Para controlar o acesso aos recursos da sua empresa e gerenciar o uso da licença, você pode ver uma lista de todas as pessoas que têm acesso à sua empresa.

Você pode ver todos os integrantes atuais da empresa e administradores da empresa{% ifversion ghec %}, bem como convites pendentes para se tornarem integrantes e administradores{% endif %}. Para facilitar o consumo destas informações, você pode pesquisar e filtrar as listas.

## Visualizando os administradores corporativos

Você pode visualizar todos os atuais proprietários da empresa{% ifversion ghec %} e gerentes de cobrança{% endif %} para a sua empresa.{% if enterprise-membership-view-improvements %} Você pode ver informações úteis sobre cada administrador{% ifversion ghec %} e filtrar a lista por função{% endif %}.{% endif %} Você pode encontrar uma pessoa específica pesquisando o nome de usuário ou nome de exibição.

{% ifversion not ghae %}
Você também pode remover um administrador. For more information. consulte "[convidando pessoas para gerenciar sua empresa](/admin/user-management/managing-users-in-your-enterprise/inviting-people-to-manage-your-enterprise#removing-an-enterprise-administrator-from-your-enterprise-account)".
{% endif %}

{% data reusables.enterprise-accounts.access-enterprise %}
{% data reusables.enterprise-accounts.people-tab %}
{% data reusables.enterprise-accounts.administrators-tab %}

## Visualizando integrantes {% if enterprise-membership-view-improvements %}{% else %}e colaboradores externos{% endif %}

Você pode visualizar todos os integrantes atuais {% if enterprise-membership-view-improvements %}{% else %}ou colaboradores externos{% endif %} para a sua empresa. Você pode visualizar as informações úteis sobre cada conta e filtrar a lista de formas úteis, como por função. Ou localizar uma determinada pessoa procurando pelo nome de usuário ou o nome de exibição dela.

Você pode ver mais informações sobre o acesso da pessoa à sua empresa como, por exemplo, as organizações às quais a pessoa pertence, clicando no nome da pessoa.

{% if remove-enterprise-members %}
Você também pode remover qualquer integrante da empresa de todas as organizações pertencentes à empresa. Para obter mais informações, consulte "[Removendo um integrante da sua empresa](/admin/user-management/managing-users-in-your-enterprise/removing-a-member-from-your-enterprise)."
{% endif %}

{% data reusables.enterprise-accounts.access-enterprise %}
{% data reusables.enterprise-accounts.people-tab %}{% if enterprise-membership-view-improvements %}{% else %}
1. Como alternativa, clique em **Outside collaborators** (Colaboradores externos) para exibir uma lista deles em vez de uma lista de integrantes.

   ![Guia de colaboradores externos na página de integrantes da empresa](/assets/images/help/business-accounts/outside-collaborators-tab.png){% endif %}

{% if enterprise-membership-view-improvements %}
## Visualizando colaboradores externos

Você pode ver todos os colaboradores externos atuais da sua empresa. Você pode ver informações úteis sobre cada colaborador e filtrar a lista de formas úteis, por exemplo, por organização. Você pode encontrar um colaborador específico pesquisando o nome de usuário ou nome de exibição.

Você pode ver mais informações sobre o acesso da pessoa à sua empresa como, por exemplo, uma lista de todos os repositórios aos quais o colaborador tem acesso, clicando no nome da pessoa.

{% data reusables.enterprise-accounts.access-enterprise %}
{% data reusables.enterprise-accounts.people-tab %}
1. Em "Pessoas", clique em **Colaboradores externos**.

  ![Aba de colaboradores na barra lateral de configurações da empresa]{% ifversion ghec%}(/assets/images/help/business-accounts/outside-collaborators-tab-sidebar-dotcom.png){% else %}(/assets/images/help/business-accounts/outside-collaborators-tab-sidebar-dotcom.png){% endif %}

{% endif %}


{% ifversion ghec %}
## Visualizando convites pendentes

You can see all the pending invitations to become members, administrators, or outside collaborators in your enterprise. É possível filtrar a lista de forma útil, por exemplo, por organização. Ou localizar uma determinada pessoa procurando pelo nome de usuário ou o nome de exibição dela.

In the list of pending members, for any individual account, you can cancel all invitations to join organizations owned by your enterprise. This does not cancel any invitations for that same person to become an enterprise administrator or outside collaborator.

{% note %}

**Note:** If an invitation was provisioned via SCIM, you must cancel the invitation via your identity provider (IdP) instead of on {% data variables.product.prodname_dotcom %}.

{% endnote %}

If you use {% data variables.product.prodname_vss_ghe %}, the list of pending invitations includes all {% data variables.product.prodname_vs %} subscribers that haven't joined any of your organizations on {% data variables.product.prodname_dotcom %}, even if the subscriber does not have a pending invitation to join an organization. For more information about how to get {% data variables.product.prodname_vs %} subscribers access to {% data variables.product.prodname_enterprise %}, see "[Setting up {% data variables.product.prodname_vss_ghe %}](/billing/managing-licenses-for-visual-studio-subscriptions-with-github-enterprise/setting-up-visual-studio-subscriptions-with-github-enterprise)."

{% data reusables.enterprise-accounts.access-enterprise %}
{% data reusables.enterprise-accounts.people-tab %}
1. Em "Pessoas", clique em **Convites pendentes.**.

   ![Captura de tela da aba "Convites pendentes" na barra lateral](/assets/images/help/enterprises/pending-invitations-tab.png)
1. Optionally, to cancel all invitations for an account to join organizations owned by your enterprise, to the right of the account, click {% octicon "kebab-horizontal" aria-label="The horizontal kebab icon" %}, then click **Cancel invitation**.

   ![Screenshot of the "Cancel invitation" button](/assets/images/help/enterprises/cancel-enterprise-member-invitation.png)
1. Optionally, to view pending invitations for enterprise administrators or outside collaborators, under "Pending members", click **Administrators** or **Outside collaborators**.

   ![Screenshot of the "Members", "Administrators", and "Outside collaborators" tabs](/assets/images/help/enterprises/pending-invitations-type-tabs.png)


## Visualizando integrantes suspensos em um {% data variables.product.prodname_emu_enterprise %}

If your enterprise uses {% data variables.product.prodname_emus %}, you can also view suspended users. Suspended users are members who have been deprovisioned after being unassigned from the {% data variables.product.prodname_emu_idp_application %} application or deleted from the identity provider. Para obter mais informações, consulte[Sobre usuários gerenciados pela empresa](/admin/identity-and-access-management/managing-iam-with-enterprise-managed-users/about-enterprise-managed-users)".

{% data reusables.enterprise-accounts.access-enterprise %}
{% data reusables.enterprise-accounts.people-tab %}
1. Para ver uma lista de integrantes suspensos, acima da lista de integrantes ativos, clique em **Suspensos**. ![Captura de tela que mostra a opção "Suspenso"](/assets/images/help/enterprises/view-suspended-members.png)

{% endif %}

## Exibir usuários inativos

You can view a list of all dormant users {% ifversion ghes or ghae %} who have not been suspended and {% endif %}who are not site administrators. {% data reusables.enterprise-accounts.dormant-user-activity-threshold %} For more information, see "[Managing dormant users](/admin/user-management/managing-users-in-your-enterprise/managing-dormant-users)."

## Leia mais

- "[Funções em uma empresa](/admin/user-management/managing-users-in-your-enterprise/roles-in-an-enterprise)"
