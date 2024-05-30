# Kubernetes

# Kubernetes Cheat Sheet

## Gestión de Clúster y Contextos

1. **`kubectl config get-contexts`**
   - Lista todos los contextos disponibles.

2. **`kubectl config current-context`**
   - Muestra el contexto actual.

3. **`kubectl config use-context [contexto]`**
   - Cambia al contexto especificado.

4. **`kubectl cluster-info`**
   - Muestra información sobre el clúster.

5. **`kubectl get nodes`**
   - Lista todos los nodos en el clúster.

6. **`kubectl describe node [nodo]`**
   - Muestra detalles sobre un nodo específico.

## Gestión de Pods

7. **`kubectl get pods`**
   - Lista todos los pods en el espacio de nombres actual.

8. **`kubectl get pods -n [namespace]`**
   - Lista todos los pods en un espacio de nombres específico.

9. **`kubectl describe pod [pod]`**
   - Muestra detalles de un pod específico.

10. **`kubectl logs [pod]`**
    - Muestra los logs de un pod.

11. **`kubectl exec -it [pod] -- [comando]`**
    - Ejecuta un comando en un pod en modo interactivo.

12. **`kubectl delete pod [pod]`**
    - Elimina un pod específico.

13. **`kubectl port-forward [pod] [puerto_local]:[puerto_pod]`**
    - Reenvía un puerto local a un puerto en el pod.

14. **`kubectl cp [pod]:[ruta_origen] [ruta_destino]`**
    - Copia archivos desde y hacia un pod.

15. **`kubectl top pod [pod]`**
    - Muestra el uso de recursos de un pod.

## Gestión de Deployments

16. **`kubectl get deployments`**
    - Lista todos los deployments en el espacio de nombres actual.

17. **`kubectl describe deployment [deployment]`**
    - Muestra detalles de un deployment específico.

18. **`kubectl create deployment [nombre] --image=[imagen]`**
    - Crea un nuevo deployment con la imagen especificada.

19. **`kubectl delete deployment [deployment]`**
    - Elimina un deployment específico.

20. **`kubectl scale deployment [deployment] --replicas=[número]`**
    - Escala un deployment a un número específico de réplicas.

21. **`kubectl rollout status deployment/[deployment]`**
    - Muestra el estado del despliegue de un deployment.

22. **`kubectl rollout undo deployment/[deployment]`**
    - Revierte el último despliegue de un deployment.

23. **`kubectl set image deployment/[deployment] [contenedor]=[nueva_imagen]`**
    - Actualiza la imagen de un contenedor en un deployment.

## Gestión de Servicios

24. **`kubectl get svc`**
    - Lista todos los servicios en el espacio de nombres actual.

25. **`kubectl describe svc [servicio]`**
    - Muestra detalles de un servicio específico.

26. **`kubectl expose deployment [deployment] --type=[tipo] --port=[puerto]`**
    - Crea un servicio para exponer un deployment.

27. **`kubectl delete svc [servicio]`**
    - Elimina un servicio específico.

## Gestión de ConfigMaps y Secrets

28. **`kubectl create configmap [nombre] --from-literal=[clave]=[valor]`**
    - Crea un ConfigMap desde un literal.

29. **`kubectl create configmap [nombre] --from-file=[archivo]`**
    - Crea un ConfigMap desde un archivo.

30. **`kubectl get configmaps`**
    - Lista todos los ConfigMaps en el espacio de nombres actual.

31. **`kubectl describe configmap [configmap]`**
    - Muestra detalles de un ConfigMap específico.

32. **`kubectl delete configmap [configmap]`**
    - Elimina un ConfigMap específico.

33. **`kubectl create secret generic [nombre] --from-literal=[clave]=[valor]`**
    - Crea un Secret desde un literal.

34. **`kubectl create secret generic [nombre] --from-file=[archivo]`**
    - Crea un Secret desde un archivo.

35. **`kubectl get secrets`**
    - Lista todos los Secrets en el espacio de nombres actual.

36. **`kubectl describe secret [secret]`**
    - Muestra detalles de un Secret específico.

37. **`kubectl delete secret [secret]`**
    - Elimina un Secret específico.

## Gestión de Namespaces

38. **`kubectl get namespaces`**
    - Lista todos los espacios de nombres en el clúster.

39. **`kubectl create namespace [nombre]`**
    - Crea un nuevo espacio de nombres.

40. **`kubectl delete namespace [nombre]`**
    - Elimina un espacio de nombres específico.

41. **`kubectl config set-context --current --namespace=[nombre]`**
    - Establece el espacio de nombres predeterminado para el contexto actual.

## Gestión de Roles y RBAC

42. **`kubectl get roles`**
    - Lista todos los roles en el espacio de nombres actual.

43. **`kubectl get clusterroles`**
    - Lista todos los roles de clúster.

44. **`kubectl get rolebindings`**
    - Lista todos los enlaces de roles en el espacio de nombres actual.

45. **`kubectl get clusterrolebindings`**
    - Lista todos los enlaces de roles de clúster.

46. **`kubectl describe role [role]`**
    - Muestra detalles de un rol específico.

47. **`kubectl describe clusterrole [clusterrole]`**
    - Muestra detalles de un rol de clúster específico.

48. **`kubectl create rolebinding [nombre] --role=[role] --user=[usuario] --namespace=[namespace]`**
    - Crea un enlace de rol.

49. **`kubectl delete rolebinding [nombre]`**
    - Elimina un enlace de rol específico.

50. **`kubectl auth can-i [verbo] [recurso]`**
    - Verifica si tienes permiso para realizar una acción en un recurso.
