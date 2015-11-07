# REST

```
class ModelNameController < ApplicationController
  def show
    @record = ModelName.find(params[:id])
    respond_to do |format|
      format.html # show.html.erb
      format.json { render json: @record }
      format.xml { render xml: @record }
    end
  end
end
