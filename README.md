# yr32infra

```mermaid
graph TD;
    subgraph Cloud
    Renovate-->GitHub
    GitHub-->Renovate
    end
    
    subgraph mitou
    m_compose-cd--Polling-->GitHub
    GitHub--WebHook-->m_portainer.io
    m_compose-cd--Deploy-->m_docker
    m_portainer.io--Deploy-->m_docker
    end
      
    subgraph arch
    a_compose-cd--Polling-->GitHub
    a_compose-cd--Deploy-->a_docker
    end
```
