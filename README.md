# bash_array

```
# Declare array
export PRD_ENV=( 'prd' 'ppr' )

# in_array
function setPolicyPath(){
  if [[ ${PRD_ENV[@]} =~ "$ENV" ]]
  then
    echo "It is a PRD Policy"
    APP_PATH="secret/apps/${APP}-PRD/${ENV}"
  else
    echo "Is is a HPRD Policy"
    APP_PATH="secret/apps/${APP}-HPRD/${ENV}"
  fi
  echo "APP_PATH=$APP_PATH"
}

```
