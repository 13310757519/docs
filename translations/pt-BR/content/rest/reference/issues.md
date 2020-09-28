---
title: Problemas
redirect_from:
  - /v3/issues
versions:
  free-pro-team: '*'
  enterprise-server: '*'
---

### Custom media types for issues

These are the supported media types for issues.

    application/vnd.github.VERSION.raw+json
    application/vnd.github.VERSION.text+json
    application/vnd.github.VERSION.html+json
    application/vnd.github.VERSION.full+json

For more information about media types, see "[Custom media types](/rest/overview/media-types)."

{% for operation in currentRestOperations %}
  {% unless operation.subcategory %}{% include rest_operation %}{% endunless %}
{% endfor %}

## Responsáveis

{% for operation in currentRestOperations %}
  {% if operation.subcategory == 'assignees' %}{% include rest_operation %}{% endif %}
{% endfor %}

## Comentários

The Issue Comments API supports listing, viewing, editing, and creating comments on issues and pull requests.

Issue Comments use [these custom media types](#custom-media-types). You can read more about the use of media types in the API [here](/v3/media/).

{% for operation in currentRestOperations %}
  {% if operation.subcategory == 'comments' %}{% include rest_operation %}{% endif %}
{% endfor %}

## Eventos

The Issue Events API can return different types of events triggered by activity in issues and pull requests. The Issue Events API can return different types of events triggered by activity in issues and pull requests. For more information about the specific events that you can receive from the Issue Events API, see "[Issue event types](/developers/webhooks-and-events/issue-event-types)." For more information, see the "[Events API](/developers/webhooks-and-events/github-event-types)."

{% for operation in currentRestOperations %}
  {% if operation.subcategory == 'events' %}{% include rest_operation %}{% endif %}
{% endfor %}

## Etiquetas

{% for operation in currentRestOperations %}
  {% if operation.subcategory == 'labels' %}{% include rest_operation %}{% endif %}
{% endfor %}

## Marcos

{% for operation in currentRestOperations %}
  {% if operation.subcategory == 'milestones' %}{% include rest_operation %}{% endif %}
{% endfor %}

## Linha do tempo

The Timeline Events API can return different types of events triggered by timeline activity in issues and pull requests. The Issue Events API can return different types of events triggered by activity in issues and pull requests. For more information about the specific events that you can receive from the Issue Events API, see "[Issue event types](/developers/webhooks-and-events/issue-event-types)." For more information, see the "[GitHub Events API](/developers/webhooks-and-events/github-event-types)."

You can use this API to display information about issues and pull request or determine who should be notified of issue comments.

{% for operation in currentRestOperations %}
  {% if operation.subcategory == 'timeline' %}{% include rest_operation %}{% endif %}
{% endfor %}