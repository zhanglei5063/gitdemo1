package com.kaishengit.action;

import com.opensymphony.xwork2.ActionContext;
import com.opensymphony.xwork2.ActionSupport;
import org.apache.struts2.ServletActionContext;

import javax.servlet.ServletContext;
import javax.servlet.http.HttpServletRequest;
import javax.servlet.http.HttpServletResponse;
import javax.servlet.http.HttpSession;
import java.util.Map;

public abstract class BaseAction extends ActionSupport{

    public Map<String,Object> getSession() {
        return ActionContext.getContext().getSession();
    }

    public Map<String,Object> getApplication() {
        return ActionContext.getContext().getApplication();
    }

    public HttpServletRequest getHttpRequest() {
        return ServletActionContext.getRequest();
    }

    public HttpServletResponse getHttpResponse() {
        return ServletActionContext.getResponse();
    }

    public HttpSession getHttpSession() {
        return getHttpRequest().getSession();
    }

    public ServletContext getServletContext() {
        return getHttpRequest().getServletContext();
    }


}

