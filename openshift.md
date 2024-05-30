# OpenShift Cheat Sheet

## Gestión de Proyectos y Usuarios

1. **`oc new-project [nombre]`**
   - Crea un nuevo proyecto.

2. **`oc project [nombre]`**
   - Cambia al proyecto especificado.

3. **`oc get projects`**
   - Lista todos los proyectos.

4. **`oc delete project [nombre]`**
   - Elimina un proyecto.

5. **`oc whoami`**
   - Muestra el usuario actual.

6. **`oc login [url]`**
   - Inicia sesión en un servidor OpenShift.

7. **`oc logout`**
   - Cierra la sesión en el servidor OpenShift.

8. **`oc adm policy add-role-to-user [rol] [usuario] -n [proyecto]`**
   - Asigna un rol a un usuario en un proyecto.

9. **`oc adm policy remove-role-from-user [rol] [usuario] -n [proyecto]`**
   - Revoca un rol de un usuario en un proyecto.

10. **`oc get users`**
    - Lista todos los usuarios.

## Gestión de Pods

11. **`oc get pods`**
    - Lista todos los pods en el proyecto actual.

12. **`oc get pods -n [namespace]`**
    - Lista todos los pods en un espacio de nombres específico.

13. **`oc describe pod [pod]`**
    - Muestra detalles de un pod específico.

14. **`oc logs [pod]`**
    - Muestra los logs de un pod.

15. **`oc exec -it [pod] -- [comando]`**
    - Ejecuta un comando en un pod en modo interactivo.

16. **`oc delete pod [pod]`**
    - Elimina un pod específico.

17. **`oc rsh [pod]`**
    - Abre una shell remota en un pod.

18. **`oc cp [pod]:[ruta_origen] [ruta_destino]`**
    - Copia archivos desde y hacia un pod.

19. **`oc port-forward [pod] [puerto_local]:[puerto_pod]`**
    - Reenvía un puerto local a un puerto en el pod.

20. **`oc get pod [pod] -o yaml`**
    - Muestra la configuración YAML de un pod.

## Gestión de Deployments y Builds

21. **`oc new-app [imagen]`**
    - Crea una nueva aplicación desde una imagen.

22. **`oc get deployments`**
    - Lista todos los deployments en el proyecto actual.

23. **`oc describe deployment [deployment]`**
    - Muestra detalles de un deployment específico.

24. **`oc rollout status deployment/[deployment]`**
    - Muestra el estado del despliegue de un deployment.

25. **`oc rollout undo deployment/[deployment]`**
    - Revierte el último despliegue de un deployment.

26. **`oc set image deployment/[deployment] [contenedor]=[nueva_imagen]`**
    - Actualiza la imagen de un contenedor en un deployment.

27. **`oc start-build [buildconfig]`**
    - Inicia una nueva compilación desde una configuración de compilación.

28. **`oc get builds`**
    - Lista todas las compilaciones en el proyecto actual.

29. **`oc logs build/[build]`**
    - Muestra los logs de una compilación específica.

30. **`oc cancel-build [build]`**
    - Cancela una compilación en curso.

## Gestión de Servicios y Rutas

31. **`oc get svc`**
    - Lista todos los servicios en el proyecto actual.

32. **`oc describe svc [servicio]`**
    - Muestra detalles de un servicio específico.

33. **`oc expose svc [servicio]`**
    - Crea una ruta para exponer un servicio.

34. **`oc get route`**
    - Lista todas las rutas en el proyecto actual.

35. **`oc describe route [ruta]`**
    - Muestra detalles de una ruta específica.

36. **`oc delete route [ruta]`**
    - Elimina una ruta específica.

37. **`oc get endpoints`**
    - Lista todos los endpoints en el proyecto actual.

38. **`oc get ingress`**
    - Lista todas las reglas de ingreso en el proyecto actual.

39. **`oc describe ingress [ingreso]`**
    - Muestra detalles de una regla de ingreso específica.

40. **`oc create route edge --service=[servicio]`**
    - Crea una ruta edge (HTTPS) para un servicio.

## Gestión de ConfigMaps y Secrets

41. **`oc create configmap [nombre] --from-literal=[clave]=[valor]`**
    - Crea un ConfigMap desde un literal.

42. **`oc create configmap [nombre] --from-file=[archivo]`**
    - Crea un ConfigMap desde un archivo.

43. **`oc get configmaps`**
    - Lista todos los ConfigMaps en el proyecto actual.

44. **`oc describe configmap [configmap]`**
    - Muestra detalles de un ConfigMap específico.

45. **`oc delete configmap [configmap]`**
    - Elimina un ConfigMap específico.

46. **`oc create secret generic [nombre] --from-literal=[clave]=[valor]`**
    - Crea un Secret desde un literal.

47. **`oc create secret generic [nombre] --from-file=[archivo]`**
    - Crea un Secret desde un archivo.

48. **`oc get secrets`**
    - Lista todos los Secrets en el proyecto actual.

49. **`oc describe secret [secret]`**
    - Muestra detalles de un Secret específico.

50. **`oc delete secret [secret]`**
    - Elimina un Secret específico.
